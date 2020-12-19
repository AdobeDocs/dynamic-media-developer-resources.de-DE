---
description: 'null'
seo-description: 'null'
seo-title: Ereignis-Rückrufe
solution: Experience Manager
title: Ereignis-Rückrufe
topic: Dynamic media
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Ereignis-Rückrufe{#event-callbacks}

Der Viewer unterstützt JavaScript-Ereignis-Rückrufe, die die Webseite zur Verfolgung des Viewer-Initialisierungsprozesses oder -Laufzeitverhaltens verwendet.

Callback-Handler werden zugewiesen, indem Ereignis und entsprechende Handler-Funktionen mit der Eigenschaft `handlers` an das JSON-Objekt `config` im Konstruktor des Viewers übergeben werden. Alternativ kann die API-Methode `setHandlers()` verwendet werden.

Folgende Viewer-Ereignis werden unterstützt:

* `initComplete` - wird ausgelöst, wenn die Viewer-Initialisierung abgeschlossen ist und alle internen Komponenten erstellt wurden, sodass die  `getComponent()` API verwendet werden kann. Der Callback-Handler nimmt keine Argumente an.
* `trackEvent` - löst jedes Mal aus, wenn ein Ereignis im Viewer auftritt, das von einem Ereignis-Tracking-System wie Adobe Analytics verarbeitet werden kann. Der Callback-Handler akzeptiert die folgenden Argumente:

   * `objID {String}` nicht verwendet.
   * `compClass {String}` nicht verwendet.
   * `instName {String}` einem Instanznamen der Viewer-SDK-Komponente, die das Ereignis ausgelöst hat.
   * `timeStamp {Number}` Zeitstempel des Ereignisses.
   * `eventInfo {String}` ereignis-Nutzlast.

* `quickViewActivate` - wird ausgelöst, wenn ein Benutzer auf ein interaktives Farbfeld innerhalb der Komponente für interaktive Farbfelder oder im Bildschirm &quot;Aktionsaufruf&quot;am Ende der Videowiedergabe klickt oder tippt. Der Callback-Handler akzeptiert das einzige Argument, bei dem es sich um ein JSON-Objekt mit den folgenden Feldern handelt:

   * `sku` {  `String`} SKU-Wert, der mit dem interaktiven Muster verknüpft ist.
   * `<additionalVariable>` {  `String`} Null oder mehr zusätzliche Variablen, die mit dem interaktiven Muster verknüpft sind.

Siehe auch [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) und [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
