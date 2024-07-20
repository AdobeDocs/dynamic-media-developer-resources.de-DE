---
description: Namespace des Viewer-SDK
solution: Experience Manager
title: Namespace des Viewer-SDK
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Namespace des Viewer-SDK{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. In den meisten Fällen muss die Web-Seite nicht direkt mit der SDK-Komponenten-API interagieren. Alle allgemeinen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Webseite mithilfe der Viewer-API `getComponent()` einen Verweis auf eine interne SDK-Komponente erhält und dann die gesamte Flexibilität der SDK-APIs selbst nutzt.

Der Namespace, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in AEM (Adobe Experience Manager) ausgeführt wird, lädt der Viewer SDK-Komponenten in den Namespace `s7viewers.s7sdk` . Und der von Dynamic Media Classic bereitgestellte Viewer lädt das SDK in `s7classic.s7sdk`.

In beiden Fällen hat der vom SDK im Viewer verwendete Namespace entweder `s7viewers` oder `s7classic` als Präfix. Außerdem unterscheidet er sich vom einfachen Namespace `s7sdk` , der im SDK-Benutzerhandbuch oder in der SDK-API-Dokumentation verwendet wird.

Daher ist es wichtig, beim Schreiben von benutzerdefiniertem Anwendungs-Code, der mit internen Viewer-Komponenten kommuniziert, einen vollständig qualifizierten SDK-Namespace zu verwenden.

Wenn Sie beispielsweise das Ereignis `StatusEvent.NOTF_VIEW_READY` überwachen möchten und der Viewer von Dynamic Media Classic bereitgestellt wird, ist der vollständig qualifizierte Ereignistyp `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` und der Ereignis-Listener-Code sieht in etwa wie folgt aus:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
