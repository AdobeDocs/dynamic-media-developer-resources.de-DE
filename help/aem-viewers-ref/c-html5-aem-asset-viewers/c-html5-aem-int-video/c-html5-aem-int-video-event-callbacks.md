---
title: Ereignis-Callbacks
description: Ereignis-Callbacks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
TQID: 'https://experienceleague.adobe.com/pAXI43BvGyX7rM3--kuoLsAsexeM993-WKoLPCU9Zzg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
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

* `quickViewActivate` : Trigger, wenn ein Benutzer in der interaktiven Farbfeldkomponente oder auf dem Bildschirm &quot;call to action&quot; am Ende der Videowiedergabe auf ein interaktives Farbfeld klickt oder tippt. Der Callback-Handler verwendet als einziges Argument ein JSON-Objekt mit den folgenden Feldern:

   * `sku` { `String`} SKU-Wert, der mit dem interaktiven Farbfeld verknüpft ist.
   * `<additionalVariable>` { `String`} Null oder mehr zusätzliche Variablen, die mit dem interaktiven Farb-/Bildmuster verknüpft sind.

Siehe auch [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) und [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
