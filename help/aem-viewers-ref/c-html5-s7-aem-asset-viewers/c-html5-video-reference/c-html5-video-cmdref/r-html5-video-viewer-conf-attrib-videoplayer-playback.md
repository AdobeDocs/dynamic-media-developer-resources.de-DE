---
description: Konfigurationsattribut für Video-Viewer.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut für Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den vom Viewer verwendeten Wiedergabetyp fest. Wenn <span class="codeph"> auto</span> auf den meisten Desktop-Browsern und auf allen iOS-Geräten festgelegt ist, verwendet der Viewer HTML5-Streaming-Videos im HLS-Format. Auf bestimmten Systemen wie älteren Internet Explorer- und Android-Systemen wird auf die progressive HTML5-Wiedergabe zurückgegriffen. </p> <p>Wenn <span class="codeph"> progressiv</span> angegeben ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, die von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Wiedergabenauswahl im automatischen und progressiven Modus finden Sie im Benutzerhandbuch für das Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

Wird ignoriert, wenn der Viewer mit externen Videos arbeitet. Siehe [Externe Video-Unterstützung](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
