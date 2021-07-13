---
description: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: 2ec6d871-05d9-4d85-b031-e64386f5d2e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklicks/Tippen zum Umschalten von Wiedergabe/Pause. Wird auf <span class="codeph"> none</span> gesetzt, wird der einmalige Klick/Tippen zum Abspielen/Anhalten deaktiviert. Wenn auf <span class="codeph"> playPause</span> gesetzt, wird beim Klicken auf das Video zwischen Wiedergabe und Pause umgeschaltet. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall ist das Verhalten <span class="codeph"> singleclick</span> deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`
