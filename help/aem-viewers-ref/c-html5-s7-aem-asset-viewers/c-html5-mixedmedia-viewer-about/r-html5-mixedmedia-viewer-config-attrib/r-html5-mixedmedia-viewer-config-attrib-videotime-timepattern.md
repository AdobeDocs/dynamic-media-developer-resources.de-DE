---
description: 'null'
seo-description: 'null'
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 5%

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Steuerungsleiste angezeigt wird, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> Minuten und <span class="codeph"> s</span> Sekunden beträgt. </p> <p>Die Anzahl der Buchstaben, die für jede Zeiteinheit verwendet werden, bestimmt die Anzahl der Stellen, die für die Einheit angezeigt werden sollen. Wenn die Zahl nicht in die angegebene Zahl passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird als Zeitmuster <span class="codeph"> m:ss</span> 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das angegebene Zeitmuster <span class="codeph"> h:mm:s</span> lautet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
