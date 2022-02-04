---
title: VideoTime.timepattern
description: Konfigurationsattribut für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1fe2876c-c59a-4e0c-b429-34cc3244d920
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

Konfigurationsattribut für Video-Viewer.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Steuerleiste angezeigt wird, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> Minuten beträgt und <span class="codeph"> s</span> ist Sekunden. </p> <p>Die Anzahl der für jede Zeiteinheit verwendeten Buchstaben bestimmt die Anzahl der für die Einheit anzuzeigenden Ziffern. Wenn die Zahl nicht in die angegebenen Ziffern passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird das Zeitmuster <span class="codeph"> m:ss</span> wird als 67:05 angezeigt. Die gleiche Zeit wird als 1 angezeigt:07:5 , wenn das angegebene Zeitmuster <span class="codeph"> h:mm:s</span>. </p> </td> 
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
