---
description: Gibt an, ob der Viewer mit dem Laden von Videoinhalten vor den Wiedergabe-Beginn beginnt.
seo-description: Gibt an, ob der Viewer mit dem Laden von Videoinhalten vor den Wiedergabe-Beginn beginnt.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
topic: Dynamic media
uuid: d080465d-7349-4671-aaa4-c49e549d1f64
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.preload{#videoplayer-preload}

Gibt an, ob der Viewer mit dem Laden von Videoinhalten vor den Wiedergabe-Beginn beginnt.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Bei Einstellung auf <span class="codeph"> 1 beginnt </span> der Download des Videos unmittelbar nach dem Festlegen des Assets; Andernfalls müssen Beginn erst dann vorgeladen werden, wenn die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Wenn auf <span class="codeph"> 0 gesetzt, funktionieren </span> bestimmte Funktionen möglicherweise erst bei Wiedergabe-Beginn. Der Suchvorgang aktualisiert den Videoframe nicht. Wenn das Standbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Videobilds angezeigt. </p> <p>Beachten Sie, dass die Deaktivierung der Videovorladung in bestimmten Versionen von Internet Explorer 11 und Edge möglicherweise ignoriert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
