---
description: Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Wenn der Wert auf <span class="codeph"> 1 </span> festgelegt ist, beginnt das Video mit dem Download, unmittelbar nachdem das Asset festgelegt wurde. Andernfalls beginnt das Vorausfüllen erst, nachdem die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Wenn auf <span class="codeph"> 0 </span> festgelegt, funktionieren bestimmte Funktionen möglicherweise erst nach dem Start der Wiedergabe. Der Suchvorgang aktualisiert den Video-Frame nicht. Wenn das Standbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Video-Frames angezeigt. </p> <p>Beachten Sie, dass die Deaktivierung der Videovorladung in bestimmten Versionen von Internet Explorer 11 und Edge-Browsern ignoriert werden kann. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
