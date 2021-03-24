---
description: Konfigurationsattribut für Video Viewer.
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic, Viewer, SDK/API, Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 5%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Konfigurationsattribut für Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert </span> </p> </td> 
   <td colname="col2"> <p>Legt die Bitrate-in-Bit-Rate für Videos pro Sekunden oder Kbit/s fest, die für die anfängliche Wiedergabe von Videos auf Desktops verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Video-Set vorhanden ist, wird der Videoplayer mit der nächstniedrigsten Bitrate Beginn. </p> <p>Bei Festlegung auf <span class="codeph"> 0 </span> wird der Videoplayer mit der niedrigstmöglichen Bitrate Beginn. Gilt nur für Systeme, die keine native Unterstützung für HTML5-HLS-Videos haben (Firefox, Chrome und Internet Explorer 11 unter Windows 10), und wenn der Wiedergabemodus auf <span class="codeph"> auto </span> eingestellt ist. </p> </td> 
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

