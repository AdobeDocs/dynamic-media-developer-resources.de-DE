---
description: JavaScript-API-Referenz für den E-Katalog-Viewer.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# setParam{#setparam}

JavaScript-API-Referenz für den E-Katalog-Viewer.

` setParam( *`name, value`*)`

Legt den Viewer-Parameter auf einen angegebenen Wert fest. Der Parameter ist entweder eine Viewer-spezifische Konfigurationsoption oder ein Modifikator des Software Development Kits. Dieser Parameter wird vor `init()` aufgerufen.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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

