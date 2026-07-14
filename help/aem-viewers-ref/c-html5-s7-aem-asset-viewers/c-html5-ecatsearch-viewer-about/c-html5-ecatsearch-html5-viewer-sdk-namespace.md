---
description: Viewer-SDK-Namespace
solution: Experience Manager
title: Viewer-SDK-Namespace
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
TQID: 'https://experienceleague.adobe.com/wS6VG2Eo73QO7-kbRLVCZ-DOrSWUb6XOB92J-zP7QV8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Viewer-SDK-Namespace{#viewer-sdk-namespace}

Der Viewer besteht aus vielen Viewer-SDK-Komponenten. In den meisten Fällen muss die Web-Seite nicht direkt mit der SDK-Komponenten-API interagieren. Alle gängigen Anforderungen werden in der Viewer-API selbst behandelt.

Einige erweiterte Anwendungsfälle erfordern jedoch, dass die Web-Seite einen Verweis auf eine SDK-Innenkomponente mithilfe der `getComponent()` Viewer-API abruft und dann die gesamte Flexibilität der APIs von SDK selbst nutzt.

Der Namespace, der zum Laden und Initialisieren von SDK-Komponenten durch den Viewer verwendet wird, hängt von der Umgebung ab, in der der Viewer ausgeführt wird. Wenn der Viewer in AEM (Adobe Experience Manager) ausgeführt wird, lädt der Viewer SDK-Komponenten in `s7viewers.s7sdk` Namespace. Und der Viewer, der von Dynamic Media Classic bereitgestellt wird, lädt den SDK in `s7classic.s7sdk`.

In beiden Fällen hat der von der SDK im Viewer verwendete Namespace entweder `s7viewers` oder `s7classic` als Präfix. Außerdem unterscheidet er sich vom einfachen `s7sdk`-Namespace, der im SDK-Benutzerhandbuch oder in der Dokumentation zur SDK-API verwendet wird.

Daher ist es wichtig, einen vollqualifizierten SDK-Namespace zu verwenden, wenn Sie benutzerdefinierten Anwendungs-Code schreiben, der mit internen Viewer-Komponenten kommuniziert.

Wenn Sie beispielsweise `StatusEvent.NOTF_VIEW_READY` Ereignis überwachen möchten und der Viewer von Dynamic Media Classic bereitgestellt wird, ist der vollständig qualifizierte Ereignistyp `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` und der Ereignis-Listener-Code sieht in etwa wie folgt aus:

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

