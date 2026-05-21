---
title: VideoScrubber.timepattern
description: Konfigurationsattribut für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e0956a0b-4d82-475f-8990-8b059014233a
TQID: 'https://experienceleague.adobe.com/9fWQxrCEXORmIq381mLddIuvjAbxDNar746L3wbrw0k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Konfigurationsattribut für Video Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die in der Zeitblase angezeigte Zeit fest, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> Minuten und <span class="codeph"> s</span> Sekunden ist. </p> <p>Die für jede Zeiteinheit verwendete Buchstabenanzahl bestimmt die Anzahl der für das Gerät anzuzeigenden Stellen. Wenn die Zahl nicht in die angegebenen Ziffern passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird das Zeitmuster <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das angegebene Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
