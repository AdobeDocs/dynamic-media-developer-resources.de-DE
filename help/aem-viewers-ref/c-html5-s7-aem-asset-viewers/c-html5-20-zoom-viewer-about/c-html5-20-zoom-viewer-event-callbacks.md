---
description: 'null'
seo-description: 'null'
seo-title: Ereignis-Rückrufe
solution: Experience Manager
title: Ereignis-Rückrufe
topic: Dynamic media
uuid: 325a3ccf-bae9-46f6-b3d0-70041a9548bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ereignis-Rückrufe{#event-callbacks}

Der Viewer unterstützt JavaScript-Ereignis-Rückrufe, die die Webseite zur Verfolgung des Viewer-Initialisierungsprozesses oder -Laufzeitverhaltens verwendet.

Callback-Handler werden zugewiesen, indem Ereignis und entsprechende Handler-Funktionen mit der `handlers` Eigenschaft an das `config` JSON-Objekt im Viewer-Konstruktor übergeben werden. Alternativ kann auch die `setHandlers()` API-Methode verwendet werden.

Folgende Viewer-Ereignis werden unterstützt:

* `initComplete` - wird ausgelöst, wenn die Viewer-Initialisierung abgeschlossen ist und alle internen Komponenten erstellt wurden, sodass die `getComponent()` API verwendet werden kann. Der Callback-Handler nimmt keine Argumente an.

* `trackEvent` - löst jedes Ereignis im Viewer aus, das von einem Ereignis-Verfolgungssystem wie Adobe Analytics verarbeitet werden kann. Der Callback-Handler akzeptiert die folgenden Argumente:

   * `objID {String}` nicht verwendet.
   * `compClass {String}` nicht verwendet.
   * `instName {String}` einem Instanznamen der Viewer-SDK-Komponente, die das Ereignis ausgelöst hat.
   * `timeStamp {Number}` Zeitstempel des Ereignisses.
   * `eventInfo {String}` Ereignis-Nutzlast.

Siehe auch [ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) und [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
