---
description: Konfigurationsattribut für Video360 Viewer.
seo-description: Konfigurationsattribut für Video360 Viewer.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

Konfigurationsattribut für Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. </p> <p>Wenn " <span class="codeph"> auto</span> "festgelegt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten das HTML5-Streaming-Video im HLS-Format und kehrt auf bestimmten Systemen wie älteren Internet Explorer- und Android-Systemen zur progressiven HTML5-Wiedergabe zurück. </p> <p>Wenn " <span class="codeph"> Progressiv</span> "festgelegt ist, verwendet der Viewer nur die HTML5-Wiedergabe, die von Browsern nativ unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weitere Informationen zur Auswahl der Wiedergabe im <span class="codeph"> automatischen</span> und <span class="codeph"> progressiven</span> nativen Modus finden Sie im HTML5 Viewers SDK Benutzerhandbuch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional. Wird ignoriert, wenn der Viewer mit externen Videos funktioniert.

Weitere Informationen finden Sie unter [Externe Videounterstützung](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) .

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
