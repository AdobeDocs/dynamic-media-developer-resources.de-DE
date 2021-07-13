---
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: 37d14494-cdb2-45f7-96e2-d7a9e90edad3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# setHandlers{#sethandlers}

JavaScript-API-Referenz für Video-Viewer.

`setHandlers(handlers)`

Gibt null oder mehr Callback-Handler an. Ein Aufruf dieser Methode überschreibt vollständig die Ereignishandler, die zuvor für diese Viewer-Instanz zugewiesen wurden. Muss vor `init()` aufgerufen werden.

## Parameter {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Handler  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert ein JavaScript-Funktionsverweis auf einen entsprechenden Rückruf ist. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Ereignis-Rückrufe </a> . </p> </td> 
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
