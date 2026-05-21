---
title: video360player.progressivebitrate
description: Konfigurationsattribut für Video360-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
TQID: 'https://experienceleague.adobe.com/Hn-KzfsFcpgPY4V66gMvEZ0avivukDTEzW-ul3uO1Po'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# video360player.progressivebitrate{#video-player-progressivebitrate}

Konfigurationsattribut für Video360-Viewer.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Wert</span> </p> </td> 
   <td colname="col2"> <p> Gibt die gewünschte Video-Bitrate (in Kilobit pro Sekunde oder kBit/s) an, die bei einem adaptiven Videoset wiedergegeben werden soll, falls das aktuelle System die adaptive Videowiedergabe nicht unterstützt. </p> <p>Die Komponente empfängt den Videostream mit der nächstmöglichen (aber nicht höheren) Bitrate zum spezifizierten Wert. Wenn alle Videostreams im adaptiven Videoset eine höhere Qualität als den angegebenen Wert aufweisen, wählt die Logik die Bitrate mit der niedrigsten Qualität aus. </p> </td> 
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
