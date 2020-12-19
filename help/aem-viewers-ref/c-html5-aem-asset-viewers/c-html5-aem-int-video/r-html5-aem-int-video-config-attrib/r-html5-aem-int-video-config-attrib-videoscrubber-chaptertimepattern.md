---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic media
uuid: bb021ecb-e169-4cf1-b121-7289311353ed
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Titelleiste der Kapitelliste angezeigt wird, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> für Minuten und <span class="codeph"> s</span> für Sekunden darstellt. </p> <p>Die Anzahl der Buchstaben, die für jede Zeiteinheit verwendet werden, bestimmt die Anzahl der Stellen, die für die Einheit angezeigt werden sollen. Wenn die Zahl nicht in die angegebene Zahl passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird ein Zeitmuster von <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```

