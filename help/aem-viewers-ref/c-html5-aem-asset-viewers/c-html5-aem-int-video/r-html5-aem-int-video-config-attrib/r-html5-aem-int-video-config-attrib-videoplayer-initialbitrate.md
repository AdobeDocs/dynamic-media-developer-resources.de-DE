---
title: VideoPlayer.initialBitrate
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
TQID: 'https://experienceleague.adobe.com/UND2NsxA0NTd9-AIt-QcrYA42SPW49wb4KEeEMTd-no'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# VideoPlayer.initialBitrate{#videoplayer-initialbitrate}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert</span> </p> </td> 
   <td colname="col2"> <p> Legt die Video-Bitrate (in Kilobit pro Sekunde oder kbps) fest, die für die anfängliche Wiedergabe von Videos auf einem Desktop verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Videoset vorhanden ist, beginnt der Video-Player mit dem Video, das die nächstniedrigere Bitrate aufweist. </p> <p>Bei <span class="codeph"> 0</span> beginnt der Video-Player mit der niedrigstmöglichen Bitrate. </p> <p>Gilt nur für Systeme, die keine native Unterstützung für HTML5 HLS-Videos haben (z. B. Browser Firefox, Chrome und Internet Explorer 11 unter Windows 10), und wenn der Wiedergabemodus auf „Auto“ eingestellt ist. </p> </td> 
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
