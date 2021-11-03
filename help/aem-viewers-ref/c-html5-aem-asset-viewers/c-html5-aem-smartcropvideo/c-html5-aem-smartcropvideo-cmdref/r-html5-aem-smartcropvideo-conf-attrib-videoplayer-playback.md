---
description: Konfigurationsattribut für Smart Crop Video Viewer.
solution: Experience Manager
title: SmartCropVideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Konfigurationsattribut für Smart Crop Video Viewer.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den vom Viewer verwendeten Wiedergabetyp fest. Wann <span class="codeph"> auto</span> festgelegt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten HTML5-Streaming-Videos im HLS-Format. Auf einigen Systemen wie älteren Internet Explorer- und Android-Geräten wird die progressive HTML5-Wiedergabe unterstützt. </p> <p>Wenn <span class="codeph"> progressiv</span> festgelegt ist, nutzt der Viewer nur die HTML5-Wiedergabe, die nativ von Browsern unterstützt wird, und gibt das Video progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Wiedergabenauswahl im automatischen und progressiven Modus finden Sie im Benutzerhandbuch für das Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

Wird ignoriert, wenn der Viewer mit externen Videos arbeitet. Siehe [Externe Videounterstützung]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
