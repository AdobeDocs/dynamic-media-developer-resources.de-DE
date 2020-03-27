---
description: Konfigurationsattribut für Video Viewer.
seo-description: Konfigurationsattribut für Video Viewer.
seo-title: VideoPlayer.play
solution: Experience Manager
title: VideoPlayer.play
topic: Dynamic media
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.play{#videoplayer-playback}

Konfigurationsattribut für Video Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. Wenn " <span class="codeph"> auto</span> "festgelegt ist, verwendet der Viewer auf den meisten Desktop-Browsern und allen iOS-Geräten das HTML5-Streaming-Video im HLS-Format. Auf bestimmten Systemen wie älteren Internet Explorer und Android wird die progressive HTML5-Wiedergabe zurückgeführt. </p> <p>Wenn <span class="codeph"> Progressiv</span> angegeben ist, verwendet der Viewer nur die HTML5-Wiedergabe, wie sie von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen ab. </p> <p>Weitere Informationen zur Auswahl der Wiedergabe im Auto- und progressiven Modus finden Sie im Viewer SDK-Benutzerhandbuch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

Wird ignoriert, wenn der Viewer mit externen Videos funktioniert. Siehe [Unterstützung](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)für externe Videos.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

