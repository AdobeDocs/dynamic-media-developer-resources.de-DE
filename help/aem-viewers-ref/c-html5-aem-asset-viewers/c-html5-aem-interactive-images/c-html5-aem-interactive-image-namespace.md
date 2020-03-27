---
description: 'null'
seo-description: 'null'
seo-title: Viewer SDK-Namensraum
solution: Experience Manager
title: Viewer SDK-Namensraum
topic: Dynamic media
uuid: e1639806-3052-4913-aae0-ca9a79100d0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Viewer SDK-Namensraum{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. In den meisten Fällen muss die Webseite nicht direkt mit der SDK-Komponenten-API interagieren. alle allgemeinen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Webseite einen Verweis auf eine interne SDK-Komponente mithilfe der `getComponent()` Viewer-API abruft und dann die gesamte Flexibilität der APIs von SDK selbst verwendet.

Der Namensraum, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in AEM (Adobe Experience Manager) ausgeführt wird, lädt der Viewer SDK-Komponenten in `s7viewers.s7sdk` Namensraum. Der vom Scene7 Publishing System bereitgestellte Viewer lädt das SDK in `s7classic.s7sdk`.

In beiden Fällen hat der vom SDK im Viewer verwendete Namensraum entweder `s7viewers` oder `s7classic` als Präfix. Und es unterscheidet sich vom einfachen `s7sdk` Namensraum, der im SDK-Benutzerhandbuch oder der SDK-API-Dokumentation verwendet wird.

Daher ist es wichtig, einen voll qualifizierten SDK-Namensraum zu verwenden, wenn Sie benutzerdefinierten Anwendungscode schreiben, der mit internen Viewer-Komponenten kommuniziert.

Wenn Sie beispielsweise planen, auf `StatusEvent.NOTF_VIEW_READY` Ereignis zu hören und der Viewer von AEM bereitgestellt wird, ist der voll qualifizierte Ereignistyp `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`und der Ereignis-Listener-Code sieht wie folgt aus:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

