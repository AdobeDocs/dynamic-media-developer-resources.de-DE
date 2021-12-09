---
title: setAsset
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# setAsset{#setasset}

JavaScript-API-Referenz für Video-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Zeichenfolge </span>} neue Asset-ID oder explizite Bildset mit optionalen Image Serving-Modifikatoren angehängt nach <span class="codeph"> ? </span>. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt ein neues Asset fest. Sie können diesen Parameter jederzeit vor oder nach `init()`. Wenn es nach aufgerufen wird `init()`, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelverweis auf ein in einem Katalog definiertes Bildset:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Explizites Bildset mit vorkombinierten Seiten:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Explizites Bildset mit individuellen Seitenbildern:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Der Scharfzeichnungsmodifikator wurde allen Bildern im Set hinzugefügt:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
