---
description: JavaScript-API-Referenz für einfachen Zoom-Viewer.
seo-description: JavaScript-API-Referenz für einfachen Zoom-Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 9e3fa66f-2817-4969-9532-99cd75b3e22a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

JavaScript-API-Referenz für einfachen Zoom-Viewer.

` setParam( *`name, value`*)`

Legt den Viewer-Parameter auf einen angegebenen Wert fest. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Modifikator des Software Development Kits. Dieser Parameter wird zuvor aufgerufen `init()`.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem `config` JSON-Objekt an den Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Name </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> Name des Parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> -Wert des Parameters. Der Wert kann nicht in Prozent kodiert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

