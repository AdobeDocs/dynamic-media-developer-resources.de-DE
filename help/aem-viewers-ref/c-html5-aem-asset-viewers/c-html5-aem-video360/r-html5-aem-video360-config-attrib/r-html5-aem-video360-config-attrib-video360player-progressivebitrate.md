---
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 9%

---


# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Konfigurationsattribut für Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`Wert`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert</span> </p> </td> 
   <td colname="col2"> <p> Gibt in Kbit/s (bzw. Kbit/s) die gewünschte Video-Bitrate an, die von einem adaptiven Video-Set wiedergegeben werden soll, falls das aktuelle System die adaptive Videowiedergabe nicht unterstützt. </p> <p>Die Komponente nimmt den Videostream mit der nächstmöglichen Bitrate (jedoch nicht über dem angegebenen Wert) auf. Wenn alle Videostreams im adaptiven Video-Set eine höhere Qualität als der angegebene Wert haben, wählt die Logik die Bitrate mit der niedrigsten Qualität. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```

