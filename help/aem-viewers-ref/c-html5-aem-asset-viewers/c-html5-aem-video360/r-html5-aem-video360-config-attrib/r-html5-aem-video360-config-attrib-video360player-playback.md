---
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 6%

---

# Video360Player.playback{#video-player-playback}

Konfigurationsattribut für Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den vom Viewer verwendeten Wiedergabetyp fest. </p> <p>Wenn <span class="codeph"> auto</span> festgelegt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten HTML5-Streaming-Videos im HLS-Format und greift auf bestimmte Systeme wie älteren Internet Explorer und Android auf die progressive HTML5-Wiedergabe zurück. </p> <p>Wenn <span class="codeph"> progressiv</span> festgelegt ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, die von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Wiedergabeauswahl in den nativen Modi <span class="codeph"> auto</span> und <span class="codeph"> progressiv</span> finden Sie im Benutzerhandbuch zum HTML5-Viewer-SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional. Wird ignoriert, wenn der Viewer mit externen Videos arbeitet.

Weitere Informationen finden Sie unter [Externe Videounterstützung](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) .

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
