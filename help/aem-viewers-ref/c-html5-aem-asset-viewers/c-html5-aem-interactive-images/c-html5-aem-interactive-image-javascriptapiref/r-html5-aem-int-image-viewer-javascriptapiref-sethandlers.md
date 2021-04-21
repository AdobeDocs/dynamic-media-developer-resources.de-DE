---
description: JavaScript-API-Referenz für den interaktiven Bild-Viewer
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: a5e42842-dc88-454b-8229-33a65c01bf88
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setHandlers{#sethandlers}

JavaScript-API-Referenz für den interaktiven Bild-Viewer

`setHandlers(handlers)`

Gibt 0 oder mehr Callback-Handler an. Durch einen Aufruf dieser Methode werden Ereignis-Handler, die zuvor für diese Viewer-Instanz zugewiesen wurden, vollständig überschrieben. Muss vor `init()` aufgerufen werden.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Handler  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Objekt}  </span> JSON-Objekt mit Viewer-Ereignis-Rückrufen. Der Eigenschaftsname ist der Name des unterstützten Viewer-Ereignisses. Der Eigenschaftswert ist ein JavaScript-Funktionsverweis auf einen entsprechenden Rückruf. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Ereignis-Rückrufe </a>. </p> </td> 
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
