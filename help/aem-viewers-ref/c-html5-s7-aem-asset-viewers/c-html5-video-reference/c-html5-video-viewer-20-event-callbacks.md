---
description: Ereignisrückrufe
solution: Experience Manager
title: Ereignisrückrufe
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '154'
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

Siehe auch [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) und [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
