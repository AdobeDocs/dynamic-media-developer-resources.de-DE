---
description: JavaScript-API-Referenz für Video360-Viewer
seo-description: JavaScript-API-Referenz für Video360-Viewer
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---


# setVideo{#setvideo}

JavaScript-API-Referenz für Video360-Viewer

`setVideo(videoUrl)`

Legt neues externes Video fest. Kann jederzeit aufgerufen werden, sowohl vor als auch nach `init()`. Wenn der Viewer nach `init()` aufgerufen wird, tauscht er das Video in der Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parameter {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} eine absolute URL zum neuen Video. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

