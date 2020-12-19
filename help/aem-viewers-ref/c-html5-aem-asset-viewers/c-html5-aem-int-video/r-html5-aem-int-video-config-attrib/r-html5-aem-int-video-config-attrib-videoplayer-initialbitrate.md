---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 251ab7d2-a0b5-4658-a2b8-6b39dd93dd5b
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert</span> </p> </td> 
   <td colname="col2"> <p> Legt die Video-Bitrate (in Kbit/s oder Kbit/s) fest, die für die anfängliche Wiedergabe von Videos auf einem Desktop verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Video-Set vorhanden ist, wird der Videoplayer mit dem Video mit der nächstniedrigeren Bitrate Beginn. </p> <p>Bei Festlegung auf <span class="codeph"> 0</span> wird der Videoplayer mit der niedrigstmöglichen Bitrate Beginn. </p> <p>Gilt nur für Systeme, die keine native Unterstützung für HTML5-HLS-Videos haben (z. B. Firefox, Chrome und Internet Explorer 11 unter Windows 10), und wenn der Wiedergabemodus auf auto eingestellt ist. </p> </td> 
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

