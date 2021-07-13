---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Konfigurationsattribut für interaktiven Video-Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Titelleiste der Kapitelbezeichnung angezeigt wird. Dabei steht <span class="codeph"> h</span> für Stunden, <span class="codeph"> m</span> für Minuten und <span class="codeph"> s</span> für Sekunden. </p> <p>Die Anzahl der für jede Zeiteinheit verwendeten Buchstaben bestimmt die Anzahl der für die Einheit anzuzeigenden Ziffern. Wenn die Zahl nicht in die angegebenen Ziffern passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird als Zeitmuster <span class="codeph"> m:ss</span> 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
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
