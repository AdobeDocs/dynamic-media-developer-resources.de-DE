---
title: Video360Player.initialbitrate
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Konfigurationsattribut für Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert</span> </p> </td> 
   <td colname="col2"> <p> Legt die Video-Bitrate (in Kilobit pro Sekunde oder Kbit/s) fest, die für die anfängliche Wiedergabe des Videos auf einem Desktop verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Videoset vorhanden ist, beginnt der Videoplayer mit dem Video, das die nächstniedrigere Bitrate aufweist. </p> <p>Wenn auf <span class="codeph"> 0</span> gesetzt, beginnt der Videoplayer mit der niedrigstmöglichen Bitrate. </p> <p>Gilt nur für Systeme, die keine native Unterstützung für HTML5 HLS-Videos haben (z. B. Firefox, Chrome und Internet Explorer 11 unter Windows 10) und wenn der Wiedergabemodus auf "auto"festgelegt ist. </p> </td> 
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
