---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: InteractiveSwatches.maxloadradius
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
topic: Dynamic media
uuid: 12391b8b-532f-4e68-ad60-4dbcc86d9e58
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Komponentenvorladeverhalten an. </p> <p>Bei Festlegung auf <span class="codeph"> -1</span> werden alle Muster gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Bei Festlegung auf <span class="codeph"> 0</span> werden nur sichtbare Farbfelder geladen. </p> <p>Auf <span class="codeph"><span class="varname"> preloadnbr</span></span> festlegen, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

