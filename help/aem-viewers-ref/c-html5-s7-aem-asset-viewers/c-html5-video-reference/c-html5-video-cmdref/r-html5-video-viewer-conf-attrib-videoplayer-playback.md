---
title: VideoPlayer.playback
description: Konfigurationsattribut für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut für Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

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

Wird ignoriert, wenn der Viewer mit externen Videos arbeitet. Siehe [Unterstützung externer Videos](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
