---
title: setHandlers
description: JavaScript-API-Referenz für Flyout-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 3a7b2aeb-2de5-4d4c-8974-47b6418140e6
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

JavaScript-API-Referenz für Flyout-Viewer.

`setHandlers(handlers)`

Gibt keinen oder mehr Callback-Handler an. Ein Aufruf dieser Methode überschreibt Ereignis-Handler, die zuvor für diese Viewer-Instanz zugewiesen wurden, vollständig. Muss vor dem `init()` aufgerufen werden.

## Parameter {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Handler </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Ereignis-Callbacks, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert ein JavaScript-Funktionsverweis auf einen entsprechenden Callback ist. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> </a> zu Ereignis-Callbacks . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
