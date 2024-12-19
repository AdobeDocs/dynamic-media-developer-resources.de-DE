---
title: setParam
description: JavaScript-API-Referenz für den Viewer für gemischte Medien.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 610a5a7d-1314-48bc-a640-319139d64adc
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---

# setParam{#setparam}

JavaScript-API-Referenz für den Viewer für gemischte Medien.

` setParam( *`name, value`*)`

Setzt den Viewer-Parameter auf einen angegebenen Wert. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Software Development Kit-Modifikator. Dieser Parameter wird vor dem `init()` aufgerufen. Diese Methode ist optional, wenn Informationen zur Viewer-Konfiguration mit `config` JSON-Objekt an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)

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

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
