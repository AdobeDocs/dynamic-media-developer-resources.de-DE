---
title: setParams
description: JavaScript-API-Referenz für Karussell-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 4bf3f8f8-73fe-4ab1-8005-aa49e4ffaba6
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# setParams{#setparams}

JavaScript-API-Referenz für Karussell-Viewer.

` setParams( *`params`*)`

Legt einen oder mehrere Parameter auf einen bestimmten Wert fest. Die Methodenargument-Syntax ist mit einer URL-Abfragezeichenfolge identisch. Das heißt, es stellt Name=Wert-Paare dar, getrennt durch `&`. Wie in einer Abfragezeichenfolge sind die Namen und Werte mit UTF8 prozentual kodiert. Bevor Sie `init()` aufrufen, muss dieser Parameter aufgerufen werden.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parameter {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value Parameterpaare, getrennt durch <span class="codeph"> und </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("CarouselView.fmt=png&CarouselView.iscommand=op_sharpen%3d1")
```
