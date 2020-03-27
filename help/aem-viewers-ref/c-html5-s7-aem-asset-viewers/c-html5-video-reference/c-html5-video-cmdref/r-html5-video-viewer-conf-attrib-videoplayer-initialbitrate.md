---
description: Konfigurationsattribut für Video Viewer.
seo-description: Konfigurationsattribut für Video Viewer.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: b2dde5f4-0449-4cad-a1f2-e336027f92c6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut für Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert </span> </p> </td> 
   <td colname="col2"> <p>Legt die Bitrate-in-Bit-Rate für Videos pro Sekunden oder Kbit/s fest, die für die anfängliche Wiedergabe von Videos auf Desktops verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Video-Set vorhanden ist, wird der Videoplayer mit der nächstniedrigsten Bitrate Beginn. </p> <p>Bei Festlegung auf <span class="codeph"> 0 </span> der Videoplayer-Beginn von der niedrigstmöglichen Bitrate. Gilt nur für Systeme, die keine native Unterstützung für HTML5-HLS-Videos haben (Firefox, Chrome und Internet Explorer 11 unter Windows 10), und wenn der Wiedergabemodus auf <span class="codeph"> auto eingestellt ist </span>. </p> </td> 
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

