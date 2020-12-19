---
description: JavaScript-API-Referenz für Video360-Viewer.
seo-description: JavaScript-API-Referenz für Video360-Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: c8c40e88-530f-4af8-be9a-2e88addd6907
translation-type: tm+mt
source-git-commit: 9abcdc9a45a19ea9c761eef6aef68abac33b9655
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---


# setParam{#setparam}

JavaScript-API-Referenz für Video360-Viewer.

` setParam( *`name, value`*)`

Legt den Viewer-Parameter auf einen angegebenen Wert fest. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Modifikator des Software Development Kits. Dieser Parameter wird vor `init()` aufgerufen.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben wurden.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parameter {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> Name des Parameters. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> Wert des Parameters. Der Wert kann nicht in Prozent kodiert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

