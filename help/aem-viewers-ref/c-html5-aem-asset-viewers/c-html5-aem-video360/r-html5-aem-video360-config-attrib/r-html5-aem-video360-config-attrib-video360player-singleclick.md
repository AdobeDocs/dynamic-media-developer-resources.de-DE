---
description: Konfigurationsattribut für Video360 Viewer.
seo-description: Konfigurationsattribut für Video360 Viewer.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
topic: Dynamic media
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

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

