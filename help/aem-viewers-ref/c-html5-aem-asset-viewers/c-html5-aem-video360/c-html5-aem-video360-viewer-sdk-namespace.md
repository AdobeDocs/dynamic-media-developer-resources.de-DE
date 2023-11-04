---
title: Namespace des Viewer-SDK
description: Namespace des Viewer-SDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3360a3bd-8a4a-4bf9-98bf-ada7c35c58f4
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Namespace des Viewer-SDK{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. Normalerweise muss die Web-Seite nicht direkt mit der SDK-Komponenten-API interagieren. Alle allgemeinen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Webseite mithilfe der `getComponent()` Viewer-API verwenden und dann die gesamte Flexibilität der APIs des SDK selbst nutzen.

Der Namespace, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in Adobe Experience Manager ausgeführt wird, lädt der Viewer SDK-Komponenten in `s7viewers.s7sdk` Namespace. Ebenso lädt der von Dynamic Media Classic bereitgestellte Viewer das SDK in `s7classic.s7sdk`.

In beiden Fällen hat der vom SDK im Viewer verwendete Namespace entweder `s7viewers` oder `s7classic` als Präfix. Und es unterscheidet sich von der Ebene `s7sdk` Namespace, der im SDK-Benutzerhandbuch oder in der SDK-API-Dokumentation verwendet wird.

Daher ist es wichtig, beim Schreiben von benutzerdefiniertem Anwendungs-Code, der mit internen Viewer-Komponenten kommuniziert, einen vollständig qualifizierten SDK-Namespace zu verwenden.

Wenn Sie beispielsweise `StatusEvent.NOTF_VIEW_READY` -Ereignis und der Viewer von Experience Manager aus bereitgestellt wird, lautet der vollqualifizierte Ereignistyp `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`und der Ereignis-Listener-Code sieht in etwa wie folgt aus:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
