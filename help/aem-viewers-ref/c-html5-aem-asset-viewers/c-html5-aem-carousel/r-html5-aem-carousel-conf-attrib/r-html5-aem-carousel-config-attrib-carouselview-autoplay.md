---
description: Konfigurationsattribut für Karussell-Viewer.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

Konfigurationsattribut für Karussell-Viewer.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,Dauer][,Richtung]</span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie lange die einzelnen Banner im Karussell angezeigt werden und in Richtung der automatischen Schleife. </p> <p>Für die automatische Loop-Deaktivierung auf <span class="codeph"> 0</span> setzen. </p> <p>Stellen Sie <span class="codeph"> 1</span> ein, um die automatische Schleife mit der Transition in Sekunden einzuschalten, die von <span class="codeph"> Dauer</span> gesteuert wird. </p> <p>Die Richtung der automatischen Schleife wird mit <span class="codeph"> Richtung</span> gesteuert. Die <span class="codeph">-Richtung</span> hat den Bereich zwischen <span class="codeph"> 1</span> von rechts nach links und <span class="codeph"> 0</span> von links nach rechts. </p> </td> 
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
