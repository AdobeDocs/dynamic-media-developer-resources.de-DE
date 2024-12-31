---
title: VideoPlayer.preload
description: Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.preload{#videoplayer-preload}

Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Ist hierfür <span class="codeph"> 1 festgelegt, beginnt </span> Video direkt nach dem Festlegen des Assets mit dem Herunterladen. Andernfalls beginnt der Vorabladevorgang erst, nachdem die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Bei Einstellung von <span class="codeph"> 0 funktionieren bestimmte Funktionen möglicherweise erst, wenn die Wiedergabe gestartet wird, </span> der Suchvorgang wird insbesondere nicht auf den Videoframe aktualisiert. Wenn das Posterbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Videoframes angezeigt. </p> <p>Die Deaktivierung der Videovorausladung kann bei bestimmten Versionen von Internet Explorer 11 und Edge-Browsern ignoriert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
