---
description: Konfigurationsattribut für Video-Viewer.
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut für Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert </span> </p> </td> 
   <td colname="col2"> <p>Legt die Video-Bitrate-in-Bits pro Sekunde oder KBit/s fest, die für die anfängliche Wiedergabe von Videos auf Desktops verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Videoset vorhanden ist, startet der Videoplayer das Video mit der nächstniedrigsten Bitrate. </p> <p>Wenn auf <span class="codeph"> 0 </span> gesetzt, beginnt der Videoplayer mit der niedrigstmöglichen Bitrate. Gilt nur für Systeme, die keine native Unterstützung für HTML5-HLS-Videos haben (Firefox, Chrome und Internet Explorer 11 unter Windows 10) und wenn der Wiedergabemodus auf <span class="codeph"> auto </span> festgelegt ist. </p> </td> 
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
