---
description: JavaScript-API-Referenz für den Inline-Zoom-Viewer.
seo-description: JavaScript-API-Referenz für den Inline-Zoom-Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 5bb7aebf-0a1d-4783-923d-7f7e7dcb9baa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---


# setAsset{#setasset}

JavaScript-API-Referenz für den Inline-Zoom-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} neue Asset-ID, expliziter Bildsatz oder expliziter Bildsatz mit frame-spezifischen Image Serving-Modifikatoren, mit optionalen globalen Image Serving-Modifikatoren nach <span class="codeph"> ?</span> angehängt. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

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

