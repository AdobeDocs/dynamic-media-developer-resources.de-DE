---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Wenn auf <span class="codeph"> -1</span> gesetzt, lädt die Komponente alle Karussellrahmen im Leerlauf vorab. </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, lädt die Komponente nur den derzeit sichtbaren Frame, den vorherigen und den nächsten Frame. </p> <p><span class="codeph"><span class="varname"> </span></span>preloadnbrennen definiert, wie viele unsichtbare Rahmen um den aktuell angezeigten Frame im Leerlauf vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
