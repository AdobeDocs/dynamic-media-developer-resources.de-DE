---
description: JavaScript-API-Referenz für Flyout-Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewer,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# setAsset{#setasset}

JavaScript-API-Referenz für Flyout-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} neue Asset-ID, expliziter Bildsatz oder expliziter Bildsatz mit Frame-spezifischen Image Serving-Modifikatoren, wobei optionale globale Image Serving-Modifikatoren nach <span class="codeph"> angehängt werden. ?</span>. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelbildreferenz:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Einzelverweis auf ein in einem Katalog definiertes Bildset:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explizites Bildset:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explizites Bildset mit Frame-spezifischen Image Serving-Modifikatoren:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Der Scharfzeichnungsmodifikator wurde allen Bildern im Set hinzugefügt:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
