---
title: VideoPlayer.progressiveBitrate
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
TQID: 'https://experienceleague.adobe.com/FKD3lPjlXUFjmtI8Zb9u0nrWlDa8B4wxqLOkqok6Vok'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 3%

---

# VideoPlayer.progressiveBitrate{#videoplayer-progressivebitrate}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert</span> </p> </td> 
   <td colname="col2"> <p> Gibt in Kilobit pro Sekunde (kBit/s) die gewünschte Video-Bitrate an, die von einem adaptiven Videoset wiedergegeben werden soll, falls das aktuelle System die adaptive Videowiedergabe nicht unterstützt. </p> <p>Die Komponente empfängt den Videostream mit der nächstmöglichen (aber nicht höheren) Bitrate zum spezifizierten Wert. Wenn alle Videostreams im adaptiven Videoset eine höhere Qualität als den angegebenen Wert aufweisen, wählt die Logik die Bitrate mit der niedrigsten Qualität aus. </p> </td> 
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
