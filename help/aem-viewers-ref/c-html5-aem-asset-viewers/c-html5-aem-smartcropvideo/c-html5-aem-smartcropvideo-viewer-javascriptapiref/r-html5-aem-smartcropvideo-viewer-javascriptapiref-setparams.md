---
title: setParams
description: JavaScript-API-Referenz für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# setParams{#setparams}

JavaScript-API-Referenz für Smart Crop Video Viewer.

` setParams( *`params`*)`

Legt einen oder mehrere Parameter auf einen bestimmten Wert fest. Die Methodenargument-Syntax ist mit einer URL-Abfragezeichenfolge identisch. Das heißt, es stellt Name=Wert-Paare dar, getrennt durch `&`. Dasselbe wie in einer Abfragezeichenfolge sind Namen und Werte prozentual mit UTF8 kodiert. Vor dem Aufruf `init()`, muss dieser Parameter aufgerufen werden.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den Konstruktor.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> Name=Wert Parameterpaare, durch die <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
