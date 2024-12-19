---
title: Ereignis-Callbacks
description: Ereignis-Callbacks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Ereignis-Callbacks{#event-callbacks}

Der Viewer unterstützt JavaScript-Ereignisrückrufe, die die Web-Seite verwendet, um den Viewer-Initialisierungsprozess oder das Laufzeitverhalten zu verfolgen.

Callback-Handler werden zugewiesen, indem Ereignisnamen und entsprechende Handler-Funktionen mit der `handlers`-Eigenschaft an `config` JSON-Objekt im Konstruktor des Viewers übergeben werden. Alternativ ist es möglich, `setHandlers()` API-Methode zu verwenden.

Zu den unterstützten Viewer-Ereignissen gehören die folgenden:

* `initComplete` : Trigger, wenn die Viewer-Initialisierung abgeschlossen ist und alle internen Komponenten erstellt wurden, sodass `getComponent()` API verwendet werden kann. Der Callback-Handler akzeptiert keine Argumente.

* `trackEvent` - Trigger jedes Mal, wenn ein Ereignis im Viewer auftritt, das von einem Ereignisverfolgungssystem wie Adobe Analytics verarbeitet werden kann. Der Callback-Handler akzeptiert die folgenden Argumente:

   * `objID {String}` wird zurzeit nicht verwendet.
   * `compClass {String}` wird zurzeit nicht verwendet.
   * `instName {String}` einen Instanznamen der Viewer-SDK-Komponente an, die das Ereignis ausgelöst hat.
   * Zeitstempel des `timeStamp {Number}`.
   * Payload des `eventInfo {String}`.

Siehe auch [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) und [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
