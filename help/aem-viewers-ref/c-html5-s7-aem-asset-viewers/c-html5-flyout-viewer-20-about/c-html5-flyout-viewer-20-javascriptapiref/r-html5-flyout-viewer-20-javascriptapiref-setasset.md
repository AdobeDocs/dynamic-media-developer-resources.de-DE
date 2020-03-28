---
description: JavaScript-API-Referenz für Flyout-Viewer.
seo-description: JavaScript-API-Referenz für Flyout-Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: c6f7e7e9-084a-46ff-8cff-1ecb71f7b8d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

JavaScript-API-Referenz für Flyout-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset</span></span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} neue Asset-ID, expliziter Bildsatz oder expliziter Bildsatz mit Bildserving-Modifikatoren, mit optionalen globalen Image Serving-Modifikatoren nach <span class="codeph"> ?</span>. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt das neue Asset fest. Sie können diesen Parameter jederzeit aufrufen, entweder vor oder nach `init()`. Wenn es nach `init()`dem Aufruf aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelbild-Referenz:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Einzelner Verweis auf einen Bildsatz, der in einem Katalog definiert ist:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Expliziter Bildsatz:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explizite Bildsätze mit Bildserving-Modifikatoren:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Scharfzeichnungsmodifizierer, der allen Bildern im Satz hinzugefügt wird:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```

