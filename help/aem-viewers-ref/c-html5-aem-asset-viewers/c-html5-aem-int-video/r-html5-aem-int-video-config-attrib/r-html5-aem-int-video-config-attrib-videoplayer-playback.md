---
title: videoPlayer.play
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
TQID: 'https://experienceleague.adobe.com/VnLfO1MI9EIpeoP4fpwMufyy-J2g615LOosZ4hLZlt8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 2%

---

# videoPlayer.play{#videoplayer-playback}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. </p> <p>Wenn <span class="codeph"> auto</span> festgelegt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten HTML5-Streaming-Videos im HLS-Format. Außerdem wird die progressive HTML5-Wiedergabe auf bestimmten Systemen wie dem älteren Internet Explorer und Android™ verwendet. </p> <p>Wenn <span class="codeph"> Progressive</span> festgelegt ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, wie sie nativ von Browsern unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Wiedergabeauswahl in <span class="codeph"> nativen Modi auto</span> und <span class="codeph"> progressiv </span> finden Sie im Benutzerhandbuch zu HTML5 Viewers SDK . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
