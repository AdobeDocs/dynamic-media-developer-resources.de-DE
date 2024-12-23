---
title: SmartCropVideoPlayer.playback
description: Konfigurationsattribut für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Konfigurationsattribut für den Smart Crop Video Viewer.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. Wenn <span class="codeph"> auto</span> festgelegt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten HTML5-Streaming-Videos im HLS-Format. Auf bestimmten Systemen wie dem älteren Internet Explorer und Android™ wird die progressive HTML5-Wiedergabe verwendet. </p> <p>Wenn <span class="codeph"> Progressive</span> angegeben ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, wie sie nativ von Browsern unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weiterführende Informationen zur Wiedergabeauswahl im automatischen und progressiven Modus finden Sie im Benutzerhandbuch zum Viewer-SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

Wird ignoriert, wenn der Viewer mit externen Videos arbeitet. Siehe [Unterstützung externer Videos]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
