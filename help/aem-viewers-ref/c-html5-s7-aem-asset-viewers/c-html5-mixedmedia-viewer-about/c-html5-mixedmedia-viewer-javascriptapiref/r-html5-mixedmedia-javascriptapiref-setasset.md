---
title: setAsset
description: JavaScript-API-Referenz für Viewer für gemischte Medien.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# setAsset{#setasset}

JavaScript-API-Referenz für Viewer für gemischte Medien.

` setAsset( *`asset`*[,data]))`

Legt das neue Asset und optional zusätzliche Asset-Daten fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*` - { `String`} neue Asset-ID oder explizites gemischtes Medienset, wobei optionale Image Serving-Modifikatoren nach `?` angehängt werden.

Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

`*`data`*` - { `JSON`} Speicherort der neuen Untertiteldatei.

Wenn keine Beschriftungsschaltfläche angegeben ist, ist sie in der Benutzeroberfläche nicht sichtbar. Mit diesem Parameter angegebene Untertitel gelten für das Video, das zuerst im gemischten Medienset angezeigt wird. Nachfolgende Videos werden ohne Untertitel wiedergegeben. Dieser Viewer unterstützt die folgenden Komponenten-IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponenten-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Name der Komponentenklasse des Viewer-SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage </span> </p> </td> 
   <td colname="col2"> <p>Bild, das im ersten Frame angezeigt werden soll, bevor das Video abgespielt wird. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption </span> </p> </td> 
   <td colname="col2"> <p> Speicherort der neuen Untertiteldatei. </p> <p>Wenn keine Beschriftungsschaltfläche angegeben ist, ist sie in der Benutzeroberfläche nicht sichtbar. Mit diesem Parameter angegebene Untertitel gelten für das Video, das zuerst im Medienset angezeigt wird. Nachfolgende Videos werden ohne Untertitel wiedergegeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referenz zu einzelnen Mediensätzen:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Expliziter Mediensatz:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Der Scharfzeichnungsmodifikator wurde allen Bildern im Set hinzugefügt:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
