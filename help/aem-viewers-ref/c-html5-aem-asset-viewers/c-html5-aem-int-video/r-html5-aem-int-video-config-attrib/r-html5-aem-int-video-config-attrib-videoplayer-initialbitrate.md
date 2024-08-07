---
title: VideoPlayer.initialbitrate
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut für interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Legt die Video-Bitrate (in Kilobit pro Sekunde oder Kbit/s) fest, die für die anfängliche Wiedergabe des Videos auf einem Desktop verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Videoset vorhanden ist, beginnt der Videoplayer mit dem Video, das die nächstniedrigere Bitrate aufweist. </p> <p>Wenn der Videoplayer auf <span class="codeph"> 0</span> gesetzt ist, beginnt er mit der niedrigstmöglichen Bitrate. </p> <p>Gilt nur für Systeme, die keine native Unterstützung für HTML5 HLS-Videos haben (z. B. Firefox, Chrome und Internet Explorer 11 unter Windows 10) und wenn der Wiedergabemodus auf "auto"festgelegt ist. </p> </td> 
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
