---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Wenn auf <span class="codeph"> -1</span> gesetzt, werden die Miniaturen gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Wenn auf <span class="codeph"> 0</span> gesetzt, werden nur die sichtbaren Miniaturen geladen. </p> <p>Legt <span class="codeph"><span class="varname"> preloadnbr</span></span> fest, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a3abd04c03e14c238a07349ce50d8310}

Optional.

## Standard {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Beispiel {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
