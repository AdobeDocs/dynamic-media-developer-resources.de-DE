---
title: setParam
description: JavaScript-API-Referenz für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---

# setParam{#setparam}

JavaScript-API-Referenz für Video Viewer.

` setParam( *`name, value`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> Parametername. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> Parameterwert. Der Wert darf nicht prozentual kodiert sein. </p> </td> 
  </tr> 
 </tbody> 
</table>

Setzt den Viewer-Parameter auf einen angegebenen Wert. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Software Development Kit-Modifikator. Dieser Parameter wird vor dem `init()` aufgerufen.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den -Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
