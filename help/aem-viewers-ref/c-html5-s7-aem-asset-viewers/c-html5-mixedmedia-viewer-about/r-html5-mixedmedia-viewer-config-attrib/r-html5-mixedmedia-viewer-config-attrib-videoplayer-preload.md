---
title: VideoPlayer.preload
description: Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Wenn auf <span class="codeph"> 1 </span> Das Video beginnt unmittelbar nach dem Festlegen des Assets herunterzuladen. Andernfalls beginnt das Vorausfüllen erst, nachdem die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Wenn auf <span class="codeph"> 0 </span> bestimmte Funktionen funktionieren möglicherweise erst nach dem Start der Wiedergabe; Der Suchvorgang aktualisiert den Video-Frame nicht. Wenn das Standbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Video-Frames angezeigt. </p> <p>Die Deaktivierung der Videovorladung kann in bestimmten Versionen von Internet Explorer 11 und Edge-Browsern ignoriert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
