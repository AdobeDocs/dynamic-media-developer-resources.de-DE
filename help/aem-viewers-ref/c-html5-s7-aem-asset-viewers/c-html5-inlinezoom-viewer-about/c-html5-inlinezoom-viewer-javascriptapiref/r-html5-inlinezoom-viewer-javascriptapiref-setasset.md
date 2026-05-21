---
title: setAsset
description: JavaScript-API-Referenz für Inline-Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b46ad5-90b7-49e1-a426-87fbe956f07e
TQID: 'https://experienceleague.adobe.com/-25X3APJGqrlx1F5awqzGpfSsyKBjw7xpHYMvbgqS2I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 1%

---

# setAsset{#setasset}

JavaScript-API-Referenz für Inline-Zoom-Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Assets</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} neue Asset-ID, explizites Bildset oder explizites Bildset mit Frame-spezifischen Bildbereitstellungs-Modifikatoren, an die optional globale Bildbereitstellungs-Modifikatoren nach <span class="codeph"> ?</span> angehängt werden. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach der `init()` aufrufen. Wenn es nach dem `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelbildreferenz:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Einzelner Verweis auf ein Bildset, das in einem Katalog definiert ist:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Explizites Bildset:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Explizites Bildset mit Frame-spezifischen Image-Serving-Modifikatoren:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Scharfzeichnungsmodifikator wurde allen Bildern im Set hinzugefügt:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
