---
title: Video360Player.preload
description: Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# Video360Player.preload{#video-player-preload}

Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Wenn auf <span class="codeph"> 1 </span> festgelegt, beginnt das Video direkt nach dem Festlegen des Assets herunterzuladen. Andernfalls beginnt der Vorabladevorgang erst, nachdem die Wiedergabe vom Endbenutzer oder einem API-Aufruf initiiert wurde. </p> <p>Bei einer Einstellung von <span class="codeph"> 0 </span> funktionieren bestimmte Funktionen möglicherweise erst, wenn die Wiedergabe gestartet wird. Insbesondere wird bei Suchvorgängen der Videoframe nicht aktualisiert. Wenn das Posterbild deaktiviert ist, wird der Viewer als leerer Bereich anstelle des ersten Videoframes angezeigt. </p> <p>Die Deaktivierung der Videovorausladung kann bei bestimmten Versionen von Internet Explorer 11 und Edge-Browsern ignoriert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
