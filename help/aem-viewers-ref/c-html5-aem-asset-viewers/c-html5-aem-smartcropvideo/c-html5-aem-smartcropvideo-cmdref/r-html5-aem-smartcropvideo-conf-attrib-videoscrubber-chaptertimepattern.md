---
title: VideoScrubber.chaptertimepattern
description: Konfigurationsattribut für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5552ed9e-d8fe-4723-a360-405b91e27f8e
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Konfigurationsattribut für Smart Crop Video Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Titelleiste der Videokapitelbezeichnung angezeigt wird. Der <span class="codeph"> h</span> ist Stunden, der <span class="codeph"> m</span> ist Minuten und der <span class="codeph"> s</span> ist Sekunden. </p> <p>Die Anzahl der für jede Zeiteinheit verwendeten Buchstaben bestimmt die Anzahl der für die Einheit anzuzeigenden Ziffern. Wenn die Zahl nicht in die angegebenen Ziffern passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird das Zeitmuster <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das angegebene Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
