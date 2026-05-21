---
title: setParams
description: JavaScript-API-Referenz für den Smart Crop Video Viewer.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 65461c4b-efa3-41f5-9f90-e96d129981da
TQID: 'https://experienceleague.adobe.com/P0drvnRKomJsedVFiffSW4JmnhuiqQcs4AA3hsG3cZw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 1%

---

# setParams{#setparams}

JavaScript-API-Referenz für den Smart Crop Video Viewer.

` setParams( *`params`*)`

Setzt einen oder mehrere Parameter auf einen bestimmten Wert. Die Syntax des Methodenargument ist identisch mit einer URL-Abfragezeichenfolge. Das heißt, es stellt name=value-Paare dar, die durch `&` getrennt sind. Wie in einer Abfragezeichenfolge werden Namen und Werte mit UTF8 prozentual kodiert. Bevor Sie `init()` aufrufen, muss dieser Parameter aufgerufen werden.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Parameter</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value-Parameterpaare, die durch <span class="codeph"> &amp;</span> getrennt sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
