---
title: VideoPlayer.playback
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut für interaktiven Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den vom Viewer verwendeten Wiedergabetyp fest. </p> <p>Wenn <span class="codeph"> auto</span> in den meisten Desktop-Browsern und auf allen iOS-Geräten festgelegt ist, verwendet der Viewer HTML5-Streaming-Videos im HLS-Format. Und auf bestimmte Systeme wie älteren Internet Explorer und Android™ wird auf die progressive HTML5-Wiedergabe zurückgegriffen. </p> <p>Wenn <span class="codeph"> progressiv</span> festgelegt ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, die von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Wiedergabeauswahl in den nativen Modi <span class="codeph"> auto</span> und <span class="codeph"> progressiv</span> finden Sie im Benutzerhandbuch zum HTML5-Viewer-SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
