---
description: Konfigurationsattribut für Video360 Viewer.
seo-description: Konfigurationsattribut für Video360 Viewer.
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 9%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Konfigurationsattribut für Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`Wert`*`

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

