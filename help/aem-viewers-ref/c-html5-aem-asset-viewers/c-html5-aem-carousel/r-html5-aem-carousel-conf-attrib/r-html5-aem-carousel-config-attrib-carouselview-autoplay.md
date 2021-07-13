---
description: Konfigurationsattribut für Karussell-Viewer.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

Konfigurationsattribut für Karussell-Viewer.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> Gibt die An-/Ausschaltzeit, die Dauer für die Anzeige der einzelnen Banner im Karussell und die Richtung der automatischen Schleife an. </p> <p>Für die automatische Schleife auf <span class="codeph"> 0</span> setzen. </p> <p>Legen Sie <span class="codeph"> 1</span> fest, um die automatische Schleife mit der Übergangsdauer in Sekunden zu aktivieren, die durch die <span class="codeph"> Dauer</span> gesteuert wird. </p> <p>Die Richtung der automatischen Schleife wird mit <span class="codeph"> Richtung</span> gesteuert. Die <span class="codeph"> Richtung</span> hat den Bereich zwischen <span class="codeph"> 1</span> von rechts nach links und <span class="codeph"> 0</span> von links nach rechts. </p> </td> 
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
