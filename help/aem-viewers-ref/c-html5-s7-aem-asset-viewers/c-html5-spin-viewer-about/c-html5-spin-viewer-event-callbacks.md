---
description: Ereignis-Rückrufe
solution: Experience Manager
title: Ereignis-Rückrufe
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
feature: Dynamic Media Classic, Viewer, SDK/API, Rotationssets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# Ereignis-Rückrufe{#event-callbacks}

Der Viewer unterstützt JavaScript-Ereignis-Rückrufe, die die Webseite zur Verfolgung des Viewer-Initialisierungsprozesses oder -Laufzeitverhaltens verwendet.

Callback-Handler werden zugewiesen, indem Ereignis und entsprechende Handler-Funktionen mit der Eigenschaft `handlers` an das JSON-Objekt `config` im Konstruktor des Viewers übergeben werden. Alternativ kann die API-Methode `setHandlers()` verwendet werden.

Folgende Viewer-Ereignis werden unterstützt:

* `initComplete` - Trigger, wenn die Viewer-Initialisierung abgeschlossen ist und alle internen Komponenten erstellt wurden, sodass die  `getComponent()` API verwendet werden kann. Der Callback-Handler nimmt keine Argumente an.

* `trackEvent` - Trigger jedes Mal, wenn ein Ereignis im Viewer auftritt, das von einem Ereignis-Tracking-System wie Adobe Analytics verarbeitet werden kann. Der Callback-Handler akzeptiert die folgenden Argumente:

   * `objID {String}` nicht verwendet.
   * `compClass {String}` nicht verwendet.
   * `instName {String}` einem Instanznamen der Viewer-SDK-Komponente, die das Ereignis ausgelöst hat.
   * `timeStamp {Number}` Zeitstempel des Ereignisses.
   * `eventInfo {String}` Ereignis-Nutzlast.

Siehe auch [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) und [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
