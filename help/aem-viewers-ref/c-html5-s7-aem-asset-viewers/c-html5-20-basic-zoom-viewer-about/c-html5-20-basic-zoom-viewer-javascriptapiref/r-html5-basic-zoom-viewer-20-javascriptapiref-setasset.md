---
description: JavaScript-API-Referenz für einfachen Zoom-Viewer.
seo-description: JavaScript-API-Referenz für einfachen Zoom-Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: af433f15-34a0-4867-97c5-acab47e3e008
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# setAsset{#setasset}

JavaScript-API-Referenz für einfachen Zoom-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} Neue Asset-ID, mit optionalen IS-Modifikatoren nach "?" </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelbild-Referenz:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Scharfzeichnungsmodifizierer, der allen Bildern im Satz hinzugefügt wird:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

