---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Gibt das Komponentenvorladeverhalten an. </p> <p>Bei Festlegung auf <span class="codeph"> -1</span> lädt die Komponente alle Karussell-Frames im Leerlauf vorab. </p> <p>Bei Festlegung auf <span class="codeph"> 0</span> lädt die Komponente nur den derzeit sichtbaren Rahmen, den vorherigen und den nächsten Frame. </p> <p><span class="codeph"><span class="varname"> "</span></span>preloadnbrings"definiert, wie viele unsichtbare Rahmen um den derzeit angezeigten Rahmen vorab geladen werden, wenn sie sich im Leerlauf befinden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
