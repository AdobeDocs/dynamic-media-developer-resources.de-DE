---
title: PanoramicView.iscommand
description: Konfigurationsattribut für den Panorama-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Konfigurationsattribut für den Panorama-Viewer.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Die Image-Serving-Befehlszeichenfolge, die auf das Bild angewendet wird.  Wenn er in der URL angegeben ist, stellen Sie sicher, dass Sie alle Vorkommen von <span class="codeph"> &amp;</span> und <span class="codeph"> =</span> als <span class="codeph"> %26</span> bzw. <span class="codeph"> %3D</span> HTTP-codieren. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Kein Standard.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Wenn in der Viewer-URL angegeben.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Wenn in den Konfigurationsdaten angegeben.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
