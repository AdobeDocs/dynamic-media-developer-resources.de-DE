---
title: Namespace des Viewer-SDK
description: Namespace des Viewer-SDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 1712f08c-70e6-483e-a4e5-614448f35374
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Namespace des Viewer-SDK{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. Normalerweise muss die Webseite nicht direkt mit der SDK-Komponenten-API interagieren. alle allgemeinen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Webseite mithilfe der `getComponent()` Viewer-API verwenden und dann die gesamte Flexibilität der APIs des SDK selbst nutzen.

Der Namespace, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in Adobe Experience Manager ausgeführt wird, lädt der Viewer SDK-Komponenten in `s7viewers.s7sdk` Namespace. Und der von Dynamic Media Classic bereitgestellte Viewer lädt das SDK in `s7classic.s7sdk`.

In beiden Fällen hat der vom SDK im Viewer verwendete Namespace entweder `s7viewers` oder `s7classic` als Präfix. Und es unterscheidet sich von der Ebene `s7sdk` Namespace, der im SDK-Benutzerhandbuch oder in der SDK-API-Dokumentation verwendet wird.

Daher ist es wichtig, beim Schreiben von benutzerdefiniertem Anwendungs-Code, der mit internen Viewer-Komponenten kommuniziert, einen vollständig qualifizierten SDK-Namespace zu verwenden.

Wenn Sie beispielsweise `StatusEvent.NOTF_VIEW_READY` -Ereignis und der Viewer von Experience Manager aus bereitgestellt wird, lautet der vollqualifizierte Ereignistyp `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`und der Ereignis-Listener-Code sieht in etwa wie folgt aus:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
