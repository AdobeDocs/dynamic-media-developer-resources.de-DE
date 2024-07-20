---
title: SmartCropVideoPlayer.preload
description: Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.
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

Gibt an, ob der Viewer beginnt, Videoinhalte zu laden, bevor die Wiedergabe beginnt.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Wenn der Wert auf <span class="codeph"> 1 </span> gesetzt ist, beginnt das Video herunterzuladen, nachdem das Asset festgelegt wurde. Andernfalls wird das Vorausfüllen erst gestartet, nachdem die Wiedergabe durch den Endbenutzer oder einen API-Aufruf initiiert wurde. </p> <p>Wenn auf <span class="codeph"> 0 </span> gesetzt, funktionieren bestimmte Funktionen möglicherweise erst, wenn die Wiedergabe erneut gestartet wird. Insbesondere wird der Video-Frame durch den Suchvorgang nicht aktualisiert. Wenn das Standbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Video-Frames angezeigt. </p> <p>Die Deaktivierung der Videovorladung kann bei bestimmten Versionen von Internet Explorer 11 und Edge ignoriert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
