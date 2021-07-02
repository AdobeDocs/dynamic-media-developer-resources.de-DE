---
description: Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '128'
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
