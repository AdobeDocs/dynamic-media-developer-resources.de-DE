---
description: JavaScript-API-Referenz für den E-Katalog-Viewer.
seo-description: JavaScript-API-Referenz für den E-Katalog-Viewer.
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 602fbf82-429b-443c-9163-f4d2e2b922dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---


# setHandlers{#sethandlers}

JavaScript-API-Referenz für den E-Katalog-Viewer.

[!DNL `setHandlers(handlers)`]

Gibt 0 oder mehr Callback-Handler an. Durch einen Aufruf dieser Methode werden Ereignis-Handler, die zuvor für diese Viewer-Instanz zugewiesen wurden, vollständig überschrieben. Muss vor `init()` aufgerufen werden.

## Parameter {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Handler  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert ein JavaScript-Funktionsverweis auf einen entsprechenden Rückruf ist. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Ereignis-Rückrufe </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

