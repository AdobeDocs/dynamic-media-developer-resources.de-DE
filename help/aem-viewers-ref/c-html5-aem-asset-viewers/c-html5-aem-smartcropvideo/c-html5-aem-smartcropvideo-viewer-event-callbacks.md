---
title: Ereignis-Callbacks
description: Ereignis-Callbacks
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
TQID: 'https://experienceleague.adobe.com/R1-8A1QXgy7TwEtZRMGt45D6WcM0AgqalP3wIbSCklU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
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
   * Payload des `eventInfo {String}`.

Siehe auch [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) und [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
