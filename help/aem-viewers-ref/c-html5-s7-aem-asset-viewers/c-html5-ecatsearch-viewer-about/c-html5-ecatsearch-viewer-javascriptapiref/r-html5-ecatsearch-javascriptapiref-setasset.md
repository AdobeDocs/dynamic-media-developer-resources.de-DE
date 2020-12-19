---
description: JavaScript-API-Referenz für Video-Viewer.
seo-description: JavaScript-API-Referenz für Video-Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: ab078f32-c523-4b6c-a0d6-45dd2af35b36
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---


# setAsset{#setasset}

JavaScript-API-Referenz für Video-Viewer.

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} Neue Asset-ID oder explizites Bildset mit optionalen Image Serving-Modifikatoren nach <span class="codeph"> ? </span>. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt ein neues Asset fest. Sie können diesen Parameter jederzeit vor oder nach [!DNL `init()`] aufrufen. Wenn es nach [!DNL `init()`] aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelner Verweis auf einen Bildsatz, der in einem Katalog definiert ist:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Expliziter Bildsatz mit vorab kombinierten Seiten:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Expliziter Bildsatz mit einzelnen Seitenbildern:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Scharfzeichnungsmodifizierer, der allen Bildern im Satz hinzugefügt wird:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

