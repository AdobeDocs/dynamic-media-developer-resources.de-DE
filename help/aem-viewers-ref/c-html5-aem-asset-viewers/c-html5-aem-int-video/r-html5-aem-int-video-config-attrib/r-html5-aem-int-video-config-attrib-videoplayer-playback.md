---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. </p> <p>Wenn <span class="codeph"> auto</span> eingestellt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten das HTML5-Streaming-Video im HLS-Format und kehrt auf bestimmten Systemen wie älteren Internet Explorer- und Android-Systemen zur progressiven HTML5-Wiedergabe zurück. </p> <p>Wenn <span class="codeph"> progressiv</span> eingestellt ist, verwendet der Viewer nur HTML5-Wiedergabe, wie von Browsern nativ unterstützt, und gibt Video progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Auswahl der Wiedergabe in den nativen Modi <span class="codeph"> auto</span> und <span class="codeph"> Progressiv</span> finden Sie im HTML5 Viewers SDK Benutzerhandbuch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
