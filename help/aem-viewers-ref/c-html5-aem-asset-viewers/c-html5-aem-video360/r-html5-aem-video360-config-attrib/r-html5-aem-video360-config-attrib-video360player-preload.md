---
description: Gibt an, ob der Viewer mit dem Laden von Videoinhalten vor den Wiedergabe-Beginn beginnt.
seo-description: Gibt an, ob der Viewer mit dem Laden von Videoinhalten vor den Wiedergabe-Beginn beginnt.
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
topic: Dynamic Media
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 8%

---


# Video360Player.preload{#video-player-preload}

Gibt an, ob der Viewer mit dem Laden von Videoinhalten vor den Wiedergabe-Beginn beginnt.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Bei Einstellung auf <span class="codeph"> 1 </span> beginnt das Video, direkt nach dem Festlegen des Assets herunterzuladen. Andernfalls müssen Beginn erst dann vorgeladen werden, wenn die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Bei Festlegung auf <span class="codeph"> 0 </span> funktionieren bestimmte Funktionen möglicherweise erst nach Beginn der Wiedergabe. Der Suchvorgang aktualisiert den Videoframe nicht. Wenn das Standbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Videobilds angezeigt. </p> <p>Beachten Sie, dass die Deaktivierung der Videovorladung in bestimmten Versionen von Internet Explorer 11 und Edge möglicherweise ignoriert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
