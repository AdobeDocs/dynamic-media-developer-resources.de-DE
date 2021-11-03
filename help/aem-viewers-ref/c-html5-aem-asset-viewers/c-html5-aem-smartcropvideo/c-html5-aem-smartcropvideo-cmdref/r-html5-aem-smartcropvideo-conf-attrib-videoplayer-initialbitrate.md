---
title: SmartCropVideoPlayer.initialbitrate
description: Konfigurationsattribut für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

Konfigurationsattribut für Video-Viewer.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert </span> </p> </td> 
   <td colname="col2"> <p>Legt die Video-Bitrate (in Kilobit pro Sekunde oder KBit/s) fest, die für die Erstwiedergabe von Videos auf Desktops verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Videoset vorhanden ist, startet der Videoplayer das Video mit der nächstniedrigsten Bitrate. </p> <p>Wenn auf <span class="codeph"> 0 </span>, beginnt der Videoplayer mit der niedrigstmöglichen Bitrate. Gilt nur für Systeme, die keine native Unterstützung für HTML5 HLS-Videos haben (Firefox, Chrome und Internet Explorer 11 unter Windows 10) und wenn der Wiedergabemodus auf <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
