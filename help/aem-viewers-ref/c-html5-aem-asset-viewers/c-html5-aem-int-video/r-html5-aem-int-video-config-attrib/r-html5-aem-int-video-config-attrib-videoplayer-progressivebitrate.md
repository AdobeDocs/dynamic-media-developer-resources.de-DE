---
title: VideoPlayer.progressivebitrate
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Konfigurationsattribut für interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Gibt in Kilobits pro Sekunde (Kbit/s) die gewünschte Video-Bitrate an, die von einem adaptiven Videoset wiedergegeben werden soll, falls das aktuelle System die adaptive Videowiedergabe nicht unterstützt. </p> <p>Die Komponente nimmt den Video-Stream mit der nächstmöglichen Bitrate (aber nicht über der) bis zum angegebenen Wert auf. Wenn alle Videostreams im adaptiven Videoset eine höhere Qualität als der angegebene Wert aufweisen, wählt die Logik die Bitrate mit der niedrigsten Qualität aus. </p> </td> 
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
