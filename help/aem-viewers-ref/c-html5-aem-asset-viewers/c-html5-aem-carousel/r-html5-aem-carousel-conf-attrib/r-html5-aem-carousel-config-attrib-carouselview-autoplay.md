---
title: CarouselView.AutoPlay
description: Konfigurationsattribut für den Karussell-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
TQID: 'https://experienceleague.adobe.com/LEeJUVIHLhplymrvp9IdNUWcfJz-Tl0kLffkik1GvkY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# CarouselView.AutoPlay{#carouselview-autoplay}

Konfigurationsattribut für den Karussell-Viewer.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,Dauer][,Richtung]</span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie lange ein Banner im Karussell angezeigt werden soll, und gibt die Richtung der automatischen Schleife an. </p> <p>Einstellung auf <span class="codeph"> 0</span> für automatische Schleifenabschaltung. </p> <p>Stellen Sie <span class="codeph"> 1</span> auf „Auto-Loop Ein“ mit einer Übergangsdauer in Sekunden ein, die durch <span class="codeph"> Dauer gesteuert wird</span>. </p> <p>Die Richtung der automatischen Schleife wird mit <span class="codeph"> Richtung gesteuert</span>. Die <span class="codeph"> Richtung </span> den Bereich zwischen <span class="codeph"> 1</span> rechts nach links und <span class="codeph"> 0</span> links nach rechts. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
