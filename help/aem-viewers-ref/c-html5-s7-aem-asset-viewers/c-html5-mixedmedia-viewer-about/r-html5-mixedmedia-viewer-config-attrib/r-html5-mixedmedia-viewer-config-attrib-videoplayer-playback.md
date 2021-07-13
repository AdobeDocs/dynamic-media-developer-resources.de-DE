---
description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

Konfigurationsattribut für Video-Viewer für gemischte Medien.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den vom Viewer verwendeten Wiedergabetyp fest. Wenn <span class="codeph"> auto</span> auf den meisten Desktop-Browsern und auf allen iOS-Geräten festgelegt ist, verwendet der Viewer HTML5-Streaming-Videos im HLS-Format. Auf bestimmten Systemen wie älteren Internet Explorer- und Android-Systemen wird auf die progressive HTML5-Wiedergabe zurückgegriffen. </p> <p>Wenn <span class="codeph"> progressiv</span> angegeben ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, die von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Wiedergabenauswahl im automatischen und progressiven Modus finden Sie im Benutzerhandbuch für das Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
