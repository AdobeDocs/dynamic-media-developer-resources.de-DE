---
description: Ereignisrückrufe
solution: Experience Manager
title: Ereignisrückrufe
feature: Dynamic Media Classic,Viewer,SDK/API,Rotationssets
role: Developer,User
exl-id: 26f1dd99-fee9-4a71-9ec1-cfd1e29cb886
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Ereignisrückrufe{#event-callbacks}

Der Viewer unterstützt JavaScript-Ereignis-Rückrufe, die die Webseite verwendet, um den Viewer-Initialisierungsprozess oder das Laufzeitverhalten zu verfolgen.

Callback-Handler werden zugewiesen, indem Ereignisnamen und entsprechende Handler-Funktionen mit der Eigenschaft `handlers` an das JSON-Objekt `config` im Konstruktor des Viewers übergeben werden. Alternativ kann die API-Methode `setHandlers()` verwendet werden.

Zu den unterstützten Viewer-Ereignissen zählen:

* `initComplete` - Trigger, wenn die Viewer-Initialisierung abgeschlossen ist und alle internen Komponenten erstellt werden, sodass die  `getComponent()` API verwendet werden kann. Der Callback-Handler nimmt keine Argumente an.

* `trackEvent` - Trigger jedes Mal, wenn ein Ereignis im Viewer auftritt, der von einem Ereignis-Tracking-System wie Adobe Analytics verarbeitet werden kann. Der Callback-Handler akzeptiert die folgenden Argumente:

   * `objID {String}` wird derzeit nicht verwendet.
   * `compClass {String}` wird derzeit nicht verwendet.
   * `instName {String}` einen Instanznamen der Viewer-SDK-Komponente, die das Ereignis ausgelöst hat.
   * `timeStamp {Number}` Ereigniszeitstempel.
   * `eventInfo {String}` Ereignis-Payload.

Siehe auch [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) und [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
