---
description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
seo-description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
seo-title: VideoPlayer.play
solution: Experience Manager
title: VideoPlayer.play
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.play{#videoplayer-playback}

Konfigurationsattribut für Video-Viewer für gemischte Medien.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. Wenn " <span class="codeph"> auto</span> "festgelegt ist, verwendet der Viewer auf den meisten Desktop-Browsern und allen iOS-Geräten das HTML5-Streaming-Video im HLS-Format. Auf bestimmten Systemen wie älteren Internet Explorer und Android wird die progressive HTML5-Wiedergabe zurückgeführt. </p> <p>Wenn <span class="codeph"> Progressiv</span> angegeben ist, verwendet der Viewer nur die HTML5-Wiedergabe, wie sie von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen ab. </p> <p>Weitere Informationen zur Auswahl der Wiedergabe im Auto- und progressiven Modus finden Sie im Viewer SDK-Benutzerhandbuch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
