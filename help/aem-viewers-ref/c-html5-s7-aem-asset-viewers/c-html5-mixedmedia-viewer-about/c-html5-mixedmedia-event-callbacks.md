---
description: Ereignisrückrufe
solution: Experience Manager
title: Ereignisrückrufe
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '156'
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

Siehe auch [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) und [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
