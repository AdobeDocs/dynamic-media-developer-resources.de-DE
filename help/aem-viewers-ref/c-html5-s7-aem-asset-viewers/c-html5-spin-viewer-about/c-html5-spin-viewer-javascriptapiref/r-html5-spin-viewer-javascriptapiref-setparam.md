---
title: setParam
description: JavaScript-API-Referenz für Rotationsset-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

JavaScript-API-Referenz für Rotationsset-Viewer.

` setParam( *`name, value`*)`

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

Legt den Viewer-Parameter auf einen angegebenen Wert fest. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Software Development Kit-Modifikator. Dieser Parameter wird vor `init()` aufgerufen.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
