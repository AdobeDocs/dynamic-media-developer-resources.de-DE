---
title: setParam
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b28ffb51-1091-4f2e-b12d-904218daf117
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

JavaScript-API-Referenz für Video-Viewer.

` setParam( *`name, value`*)`

Legt den Viewer-Parameter auf einen angegebenen Wert fest. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Software Development Kit-Modifikator. Dieser Parameter wird vor `init()` aufgerufen.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> Name des Parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> Wert des Parameters. Der Wert kann nicht prozentual kodiert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
