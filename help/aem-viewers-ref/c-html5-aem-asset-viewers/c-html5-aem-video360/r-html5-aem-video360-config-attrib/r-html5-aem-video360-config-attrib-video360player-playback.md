---
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---


# Video360Player.playback{#video-player-playback}

Konfigurationsattribut für Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. </p> <p>Wenn <span class="codeph"> auto</span> eingestellt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten das HTML5-Streaming-Video im HLS-Format und kehrt auf bestimmten Systemen wie älteren Internet Explorer- und Android-Systemen zur progressiven HTML5-Wiedergabe zurück. </p> <p>Wenn <span class="codeph"> progressiv</span> eingestellt ist, verwendet der Viewer nur HTML5-Wiedergabe, wie von Browsern nativ unterstützt, und gibt Video progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Auswahl der Wiedergabe in den nativen Modi <span class="codeph"> auto</span> und <span class="codeph"> Progressiv</span> finden Sie im HTML5 Viewers SDK Benutzerhandbuch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional. Wird ignoriert, wenn der Viewer mit externen Videos funktioniert.

Weitere Informationen finden Sie unter [Externe Videounterstützung](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760).

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
