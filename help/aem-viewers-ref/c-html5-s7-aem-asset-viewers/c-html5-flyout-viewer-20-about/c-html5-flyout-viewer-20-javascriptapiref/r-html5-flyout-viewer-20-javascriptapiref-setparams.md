---
title: setParams
description: JavaScript-API-Referenz für Flyout-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bd26292d-f9c6-4e67-8cc1-c74336d50860
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

JavaScript-API-Referenz für Flyout-Viewer.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> Name=Wert Parameterpaare, durch die <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt einen oder mehrere Parameter auf einen bestimmten Wert fest. Die Methodenargument-Syntax ist mit einer URL-Abfragezeichenfolge identisch. Das heißt, es stellt Name=Wert-Paare dar, getrennt durch `&`. Dasselbe wie in einer Abfragezeichenfolge sind Namen und Werte prozentual mit UTF8 kodiert. Vor dem Aufruf `init()`, muss dieser Parameter aufgerufen werden. Diese Methode ist optional, wenn Informationen zur Viewer-Konfiguration mit `config` JSON-Objekt an den Konstruktor.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
