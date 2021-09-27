---
title: Ereignisrückrufe
description: Ereignisrückrufe
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
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

* `quickViewActivate` - Trigger, wenn ein Benutzer innerhalb der interaktiven Farbfeldkomponente oder im am Ende der Videowiedergabe angezeigten Bildschirm &quot;Aktionsaufruf&quot;auf ein interaktives Muster klickt oder tippt. Der Callback-Handler akzeptiert das einzige Argument, bei dem es sich um ein JSON-Objekt mit den folgenden Feldern handelt:

   * `sku` {  `String`} SKU-Wert, der mit dem interaktiven Muster verknüpft ist.
   * `<additionalVariable>` {  `String`} Null oder mehr zusätzliche Variablen, die mit dem interaktiven Muster verknüpft sind.

Siehe auch [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) und [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
