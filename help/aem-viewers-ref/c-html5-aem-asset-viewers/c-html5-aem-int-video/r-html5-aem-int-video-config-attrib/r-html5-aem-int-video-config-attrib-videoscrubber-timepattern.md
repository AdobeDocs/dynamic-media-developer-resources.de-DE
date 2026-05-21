---
title: VideoScrubber.timepattern
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
TQID: 'https://experienceleague.adobe.com/ZNw6n5Zokz-s696GvaLkQJY-fAT-JoNafyLzpztZqos'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Zeitblase angezeigt wird, wobei <span class="codeph"> h</span> Stunden, <span class="codeph"> m</span> für Minuten und <span class="codeph"> s</span> für Sekunden darstellt. </p> <p>Die für jede Zeiteinheit verwendete Buchstabenanzahl bestimmt die Anzahl der für das Gerät anzuzeigenden Stellen. Wenn die Zahl nicht in die angegebenen Ziffern passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird ein Zeitmuster von <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
