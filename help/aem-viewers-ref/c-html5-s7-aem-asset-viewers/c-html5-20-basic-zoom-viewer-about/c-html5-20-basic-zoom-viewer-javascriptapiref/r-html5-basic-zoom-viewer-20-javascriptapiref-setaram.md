---
title: setParam
description: JavaScript-API-Referenz für Basic Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 5a34ad67-3a4c-408c-8e20-bbab87bbd470
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---

# setParam{#setparam}

JavaScript-API-Referenz für Basic Zoom Viewer.

` setParam( *`name, value`*)`

Setzt den Viewer-Parameter auf einen angegebenen Wert. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Software Development Kit-Modifikator. Dieser Parameter wird vor dem `init()` aufgerufen.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den -Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

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
