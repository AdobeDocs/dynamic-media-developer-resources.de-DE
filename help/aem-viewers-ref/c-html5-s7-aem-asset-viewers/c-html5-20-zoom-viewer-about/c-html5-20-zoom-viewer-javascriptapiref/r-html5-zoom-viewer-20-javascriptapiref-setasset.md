---
title: setAsset
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---

# setAsset{#setasset}

JavaScript-API-Referenz für Video-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} neue Asset-ID, explizites Bildset oder explizites Bildset mit bildspezifischen Image Serving-Modifikatoren, wobei optionale globale Image Serving-Modifikatoren nach "?"angehängt werden. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelbildreferenz wie folgt:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Einzelner Verweis auf ein Bildset, das wie folgt in einem Katalog definiert ist:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explizites Bildset wie folgt:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explizites Bildset mit Frame-spezifischen Image Serving-Modifikatoren wie folgt:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Der Scharfzeichnungs-Modifikator wurde wie folgt zu allen Bildern im Set hinzugefügt:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
