---
description: Konfigurationsattribut für Video360 Viewer.
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 9%

---

# Video360Player.singleclick{#video-player-singleclick}

Konfigurationsattribut für Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einfaches Klicken/Tippen zum Umschalten zwischen Wiedergabe/Pause. Wenn Sie auf <span class="codeph"> none</span> festlegen, wird Single-Click/tap zum Abspielen/Anhalten deaktiviert. Wenn auf <span class="codeph"> playPause</span> festgelegt, wird durch Klicken auf das Video zwischen dem Abspielen und Anhalten des Videos umgeschaltet. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall ist ein <span class="codeph">-Singleclick</span>-Verhalten deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
