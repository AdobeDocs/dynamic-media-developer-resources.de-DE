---
description: Viewer SDK-Namensraum
solution: Experience Manager
title: Viewer SDK-Namensraum
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 4a4d821e-9351-4efa-8849-968e746911f3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Viewer SDK-Namensraum{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. In den meisten Fällen muss die Webseite nicht direkt mit der SDK-Komponenten-API interagieren. alle allgemeinen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Webseite einen Verweis auf eine interne SDK-Komponente mit der Viewer-API `getComponent()` abruft und dann die gesamte Flexibilität der APIs des SDK selbst verwendet.

Der Namensraum, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in AEM (Adobe Experience Manager) ausgeführt wird, lädt der Viewer SDK-Komponenten in den Namensraum `s7viewers.s7sdk`. Genauso lädt der von Dynamic Media Classic bereitgestellte Viewer das SDK in `s7classic.s7sdk`.

In beiden Fällen hat der vom SDK im Viewer verwendete Namensraum entweder `s7viewers` oder `s7classic` als Präfix. Und es unterscheidet sich vom einfachen `s7sdk`-Namensraum, der im SDK-Benutzerhandbuch oder der SDK-API-Dokumentation verwendet wird.

Daher ist es wichtig, einen voll qualifizierten SDK-Namensraum zu verwenden, wenn Sie benutzerdefinierten Anwendungscode schreiben, der mit internen Viewer-Komponenten kommuniziert.

Wenn Sie beispielsweise das `StatusEvent.NOTF_VIEW_READY`-Ereignis überwachen möchten und der Viewer von AEM bereitgestellt wird, ist der voll qualifizierte Ereignistyp `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` und der Ereignis-Listener-Code sieht ähnlich wie folgt aus:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
