---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
uuid: cff2e7a4-ba88-4248-8e9f-ed1a3b628924
feature: Dynamic Media Classic, Viewer, SDK/API, Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Gibt das Komponentenvorladeverhalten an. Bei Festlegung auf <span class="codeph"> -1</span> werden alle Farbfelder gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Bei Festlegung auf <span class="codeph"> 0</span> werden nur sichtbare Farbfelder geladen. </p> <p><span class="codeph"><span class="varname"> Mit </span></span> preloadnbrs wird festgelegt, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`
