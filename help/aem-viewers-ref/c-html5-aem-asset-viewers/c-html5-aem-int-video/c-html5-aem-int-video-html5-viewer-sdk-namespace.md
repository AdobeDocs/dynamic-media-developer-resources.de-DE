---
title: Namespace des Viewer-SDK
description: Namespace des Viewer-SDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 4a4d821e-9351-4efa-8849-968e746911f3
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Namespace des Viewer-SDK{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. Normalerweise muss die Webseite nicht direkt mit der SDK-Komponenten-API interagieren. alle allgemeinen Anforderungen werden in der Viewer-API selbst behandelt.

In einigen erweiterten Anwendungsfällen muss die Web-Seite jedoch mithilfe der Viewer-API `getComponent()` auf eine interne SDK-Komponente verweisen und dann die gesamte Flexibilität der SDK-APIs selbst nutzen.

Der Namespace, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in Adobe Experience Manager ausgeführt wird, lädt der Viewer SDK-Komponenten in den Namespace `s7viewers.s7sdk` . Ebenso lädt der von Dynamic Media Classic bereitgestellte Viewer das SDK in `s7classic.s7sdk`.

In beiden Fällen hat der vom SDK im Viewer verwendete Namespace entweder `s7viewers` oder `s7classic` als Präfix. Außerdem unterscheidet er sich vom einfachen `s7sdk`-Namespace, der im SDK-Benutzerhandbuch oder in der SDK-API-Dokumentation verwendet wird.

Daher ist es wichtig, beim Schreiben von benutzerdefiniertem Anwendungs-Code, der mit internen Viewer-Komponenten kommuniziert, einen vollständig qualifizierten SDK-Namespace zu verwenden.

Wenn Sie beispielsweise das Ereignis `StatusEvent.NOTF_VIEW_READY` überwachen möchten und der Viewer vom Experience Manager bereitgestellt wird, ist der vollständig qualifizierte Ereignistyp `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` und der Ereignis-Listener-Code sieht in etwa wie folgt aus:

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
