---
title: SmartCropVideoPlayer.preload
description: Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Ist hierfür <span class="codeph"> 1 festgelegt, beginnt </span> Video direkt nach dem Festlegen des Assets mit dem Herunterladen. Andernfalls beginnt der Vorabladevorgang erst, nachdem die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Bei einer Einstellung von <span class="codeph"> 0 funktionieren bestimmte </span> möglicherweise erst, wenn die Wiedergabe erneut gestartet wird, insbesondere wird bei Suchvorgängen der Videoframe nicht aktualisiert. Wenn das Posterbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Videoframes angezeigt. </p> <p>Die Deaktivierung der Videovorausladung kann bei bestimmten Versionen von Internet Explorer 11 und Edge-Browsern ignoriert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
