---
title: Viewer-SDK-Namespace
description: Viewer-SDK-Namespace
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Viewer-SDK-Namespace{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. Normalerweise muss die Web-Seite nicht direkt mit der SDK-Komponenten-API interagieren. Alle gängigen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Web-Seite mithilfe der `getComponent()` Viewer-API auf eine innere SDK-Komponente verweist und dann die gesamte Flexibilität der APIs von SDK selbst nutzt.

Der Namespace, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in Adobe Experience Manager ausgeführt wird, lädt der Viewer SDK-Komponenten in `s7viewers.s7sdk` Namespace. Ebenso lädt der von Dynamic Media Classic bereitgestellte Viewer den SDK in `s7classic.s7sdk`.

In beiden Fällen hat der von der SDK im Viewer verwendete Namespace entweder `s7viewers` oder `s7classic` als Präfix. Außerdem unterscheidet er sich vom einfachen `s7sdk`-Namespace, der im SDK-Benutzerhandbuch oder in der Dokumentation zur SDK-API verwendet wird. Aus diesem Grund ist es wichtig, einen vollqualifizierten SDK-Namespace zu verwenden, wenn Sie benutzerdefinierten Anwendungs-Code schreiben, der mit internen Viewer-Komponenten kommuniziert.

Wenn Sie beispielsweise `StatusEvent.NOTF_VIEW_READY` Ereignis überwachen möchten und der Viewer vom Experience Manager bereitgestellt wird, ist der vollständig qualifizierte Ereignistyp `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` und der Ereignis-Listener-Code sieht in etwa wie folgt aus:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
