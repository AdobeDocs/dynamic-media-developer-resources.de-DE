---
description: Konfigurationsattribut für Video360 Viewer.
seo-description: Konfigurationsattribut für Video360 Viewer.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 73651147-d122-4466-ad74-e5f9438a9c56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

Konfigurationsattribut für Video360 Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Zeitblase angezeigt wird, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> Minuten und <span class="codeph"> s</span> Sekunden ist. </p> <p>Die Anzahl der Buchstaben, die für jede Zeiteinheit verwendet werden, bestimmt die Anzahl der Stellen, die für die Einheit angezeigt werden sollen. Wenn die Zahl nicht in die angegebene Zahl passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird das Zeitmuster <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das angegebene Zeitmuster <span class="codeph"> h:mm:s</span>ist. </p> </td> 
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

