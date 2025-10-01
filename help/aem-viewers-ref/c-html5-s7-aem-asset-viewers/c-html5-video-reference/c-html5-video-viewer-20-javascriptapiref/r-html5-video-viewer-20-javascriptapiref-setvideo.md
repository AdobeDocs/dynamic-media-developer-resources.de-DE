---
title: setVideo
description: JavaScript-API-Referenz für Video-Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# setVideo{#setvideo}

JavaScript-API-Referenz für Video-Viewer

`setVideo(videoUrl[, data])`

Legt neue externe Videodaten und optionale zusätzliche Videodaten fest. Kann jederzeit aufgerufen werden, sowohl vor als auch nach dem `init()`. Wenn der Viewer nach dem `init()` aufgerufen wird, tauscht er das Video zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)

## Parameter {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl-</span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} eine absolute URL zum neuen Video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON-Objekt mit den folgenden optionalen Feldern (von Schreibweise abhängig): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterImage </span> - Bild, das beim ersten Frame angezeigt wird, bevor das Video abgespielt wird. Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage-</a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption </span> : Speicherort der neuen Untertiteldatei. Wenn keine Untertiteldatei angegeben ist, wird die Schaltfläche für die Beschriftung nicht auf der Benutzeroberfläche angezeigt. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph">-</span> - URL oder Pfad zum WebVTT-Navigationsinhalt. Die WebVTT-Datei sollte von Image Serving bereitgestellt werden. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

<!--
## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
<instance>.setVideo("https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html")
```
-->
