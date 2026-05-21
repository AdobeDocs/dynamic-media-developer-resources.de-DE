---
title: VideoTime.timePattern
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
TQID: 'https://experienceleague.adobe.com/T2S4fAjAry5waLTPztxZjvDzVBVCoBqbfJXSZK-5SAQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# VideoTime.timePattern{#videotime-timepattern}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Legt das Muster für die Zeit fest, die in der Steuerleiste angezeigt wird. Dabei steht <span class="codeph"> h</span> für Stunden, <span class="codeph"> m</span> für Minuten und <span class="codeph"> s</span> für Sekunden. </p> <p>Die für jede Zeiteinheit verwendete Buchstabenanzahl bestimmt die Anzahl der für das Gerät anzuzeigenden Stellen. Wenn die Zahl nicht in die angegebenen Ziffern passt, wird der entsprechende Wert in der nachfolgenden Einheit angezeigt. </p> <p>Wenn die aktuelle Filmzeit beispielsweise 67 Minuten und 5 Sekunden beträgt, wird ein Zeitmuster von <span class="codeph"> m:ss</span> als 67:05 angezeigt. Die gleiche Zeit wird als 1:07:5 angezeigt, wenn das Zeitmuster <span class="codeph"> h:mm:s</span> ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
