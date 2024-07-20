---
title: setParams
description: JavaScript API-Referenz für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 65461c4b-efa3-41f5-9f90-e96d129981da
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# setParams{#setparams}

JavaScript API-Referenz für Smart Crop Video Viewer.

` setParams( *`params`*)`

Legt einen oder mehrere Parameter auf einen bestimmten Wert fest. Die Methodenargument-Syntax ist mit einer URL-Abfragezeichenfolge identisch. Das heißt, es stellt Name=Wert-Paare dar, getrennt durch `&`. Dasselbe wie in einer Abfragezeichenfolge sind Namen und Werte prozentual mit UTF8 kodiert. Bevor Sie `init()` aufrufen, muss dieser Parameter aufgerufen werden.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

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
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
