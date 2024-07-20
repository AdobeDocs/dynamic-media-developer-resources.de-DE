---
title: setAsset
description: JavaScript API-Referenz für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 70e2a0c7-8614-432a-9e20-c6d60441bb6c
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# setAsset{#setasset}

JavaScript API-Referenz für Smart Crop Video Viewer.

`setAsset(asset[, data])`

Legt das neue Asset und optional zusätzliche Asset-Daten fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcrop video/c-html5-aem-smartcrop-video-viewer-javascriptapiref\r-html5-aem-smartvideo-viewer-javascriptapiref-init.md#reference-3b57 0ba8b35045d6b30fb178c21a66c6).

## Parameter {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} neue Asset-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON-Objekt mit den folgenden optionalen Feldern (Groß-/Kleinschreibung beachten): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Bild, das im ersten Frame angezeigt wird, bevor die Videowiedergabe beginnt. Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> caption </span> - Speicherort der neuen Untertiteldatei. Wenn die Datei nicht angegeben ist, ist die Schaltfläche für die Untertitelung in der Benutzeroberfläche nicht sichtbar. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
