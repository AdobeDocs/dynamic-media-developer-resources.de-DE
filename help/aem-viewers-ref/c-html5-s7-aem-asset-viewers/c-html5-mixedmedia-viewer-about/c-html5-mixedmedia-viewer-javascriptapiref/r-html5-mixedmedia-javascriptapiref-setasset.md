---
description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---


# setAsset{#setasset}

JavaScript-API-Referenz für gemischte Medien-Viewer.

` setAsset( *`asset`*[,data]))`

Legt das neue Asset und optional zusätzliche Asset-Daten fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*`  - {  `String`} neue Asset-ID oder explizite gemischte Mediensets, mit optionalen Image Serving-Modifikatoren nach  `?`.

Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

`*`data`*` - {  `JSON`} Speicherort der neuen Untertiteldatei.

Ist dies nicht der Fall, ist die Beschriftungsschaltfläche in der Benutzeroberfläche nicht sichtbar. Die mit diesem Parameter angegebenen Bildunterschriften gelten für das Video, das zuerst im gemischten Medienset angezeigt wird. nachfolgende Videos werden ohne Bildunterschriften abgespielt. Dieser Viewer unterstützt die folgenden Komponenten-IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponenten-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Name der Viewer SDK-Komponentenklasse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Posterbild  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das im ersten Bild vor dem Abspielen des Beginns angezeigt wird. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption  </span> </p> </td> 
   <td colname="col2"> <p> Speicherort der neuen Untertiteldatei. </p> <p>Ist dies nicht der Fall, ist die Beschriftungsschaltfläche in der Benutzeroberfläche nicht sichtbar. Die mit diesem Parameter angegebenen Beschriftungen gelten für das Video, das zuerst im Medienset angezeigt wird. Nachfolgende Videos werden ohne Bildunterschriften wiedergegeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referenz zu einzelnen Mediensätzen:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Explizites Medienset:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Scharfzeichnungsmodifizierer, der allen Bildern im Satz hinzugefügt wird:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

