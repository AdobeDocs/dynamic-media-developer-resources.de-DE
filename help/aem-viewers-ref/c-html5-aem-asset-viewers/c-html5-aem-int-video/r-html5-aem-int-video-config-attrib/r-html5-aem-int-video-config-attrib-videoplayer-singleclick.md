---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut für interaktiven Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklicks/Tippen zum Umschalten von Wiedergabe/Pause. Wird auf <span class="codeph"> none</span> gesetzt, wird der einmalige Klick/Tippen zum Abspielen/Anhalten deaktiviert. Wenn auf <span class="codeph"> playPause</span> gesetzt, wird beim Klicken auf das Video zwischen Wiedergabe und Pause umgeschaltet. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall ist das Verhalten <span class="codeph"> singleclick</span> deaktiviert. </p> </td> 
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
