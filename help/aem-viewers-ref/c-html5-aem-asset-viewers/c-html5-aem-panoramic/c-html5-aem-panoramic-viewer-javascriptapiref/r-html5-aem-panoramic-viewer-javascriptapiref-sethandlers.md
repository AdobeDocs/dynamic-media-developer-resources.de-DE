---
title: setHandlers
description: JavaScript-API-Referenz für Panorama-Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 90775d4a-386b-4b56-b75e-8afafe749645
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandlers{#sethandlers}

JavaScript-API-Referenz für Panorama-Viewer

`setHandlers(handlers)`

Gibt keinen oder mehr Callback-Handler an. Ein Aufruf dieser Methode überschreibt Ereignis-Handler, die zuvor für diese Viewer-Instanz zugewiesen wurden, vollständig. Muss vor dem `init()` aufgerufen werden.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Handler </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Ereignis-Callbacks, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert ein JavaScript-Funktionsverweis auf einen entsprechenden Callback ist. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie im Abschnitt Ereignis-Callbacks . </p> </td> 
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
