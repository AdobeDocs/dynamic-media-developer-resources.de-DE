---
title: VideoPlayer.preload
description: Gibt an, ob der Viewer vor dem Start der Wiedergabe mit dem Laden von Videoinhalten beginnt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
TQID: 'https://experienceleague.adobe.com/6GudMzjM8fboYjgyb-A1HLl6TYirlrQOSjJjt5XWfnw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

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
