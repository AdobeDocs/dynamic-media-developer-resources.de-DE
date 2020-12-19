---
description: JavaScript-API-Referenz für den Inline-Zoom-Viewer.
seo-description: JavaScript-API-Referenz für den Inline-Zoom-Viewer.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 50fde4b0-2fd8-4341-bb2f-b1785f82ebc1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 1%

---


# setParams{#setparams}

JavaScript-API-Referenz für den Inline-Zoom-Viewer.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value Parameterpaare, durch  <span class="codeph"> &amp;</span> getrennt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt einen oder mehrere Parameter auf einen bestimmten Wert fest. Die Methodenargument-Syntax ist mit einer URL-Abfrage identisch. Das heißt, sie repräsentiert Paare des Typs &quot;name=Wert&quot;, die durch `&` getrennt sind. Dasselbe wie in einer Abfrage-Zeichenfolge sind Namen und Werte in Prozent mit UTF8 kodiert. Bevor Sie `init()` aufrufen, muss dieser Parameter aufgerufen werden. Diese Methode ist optional, wenn Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

