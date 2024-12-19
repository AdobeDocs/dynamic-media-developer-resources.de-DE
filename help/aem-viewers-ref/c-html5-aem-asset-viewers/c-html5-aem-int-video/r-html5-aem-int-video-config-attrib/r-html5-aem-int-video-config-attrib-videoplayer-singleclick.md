---
title: VideoPlayer.singleclick
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zum Umschalten der Wiedergabe/Pause. Wenn Sie Keine <span class="codeph">, wird </span> Ein-Klick/Tippen zur Wiedergabe/Pause deaktiviert. Wenn <span class="codeph"> PlayPause</span> festgelegt ist, wird bei Auswahl des Videos zwischen Wiedergabe und Pause des Videos umgeschaltet. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall ist ein <span class="codeph"> Einzelklick</span>Verhalten deaktiviert. </p> </td> 
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
