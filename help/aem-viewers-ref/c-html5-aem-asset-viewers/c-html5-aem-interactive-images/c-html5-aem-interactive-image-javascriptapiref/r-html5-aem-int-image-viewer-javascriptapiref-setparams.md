---
title: setParams
description: JavaScript-API-Referenz für den Videobild-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a09e3bc-e79c-4206-be42-0c6ae3d91590
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# setParams{#setparams}

JavaScript-API-Referenz für den Videobild-Viewer.

` setParams( *`params`*)`

Setzt einen oder mehrere Parameter auf einen bestimmten Wert. Die Syntax des Methodenargument ist identisch mit einer URL-Abfragezeichenfolge. Das heißt, es stellt name=value-Paare dar, die durch `&` getrennt sind. In einer Abfragezeichenfolge werden die Namen und Werte mit UTF8 prozentual codiert. Bevor Sie `init()` aufrufen, muss dieser Parameter aufgerufen werden.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den -Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

## Parameter {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Parameter</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value-Parameterpaare, die durch <span class="codeph"> und </span> getrennt sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.fmt=png&ZoomView.iscommand=op_sharpen%3d1")
```
