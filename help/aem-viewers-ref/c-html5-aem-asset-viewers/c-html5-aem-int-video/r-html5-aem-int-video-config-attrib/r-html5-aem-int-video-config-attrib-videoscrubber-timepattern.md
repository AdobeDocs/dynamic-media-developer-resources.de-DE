---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Zeitblase angezeigt wird, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> für Minuten und <span class="codeph"> s</span> für Sekunden darstellt. </p> <p>Die Anzahl der Buchstaben, die für jede Zeiteinheit verwendet werden, bestimmt die Anzahl der Stellen, die für die Einheit angezeigt werden sollen. Wenn die Zahl nicht in die angegebene Zahl passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird ein Zeitmuster von <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
