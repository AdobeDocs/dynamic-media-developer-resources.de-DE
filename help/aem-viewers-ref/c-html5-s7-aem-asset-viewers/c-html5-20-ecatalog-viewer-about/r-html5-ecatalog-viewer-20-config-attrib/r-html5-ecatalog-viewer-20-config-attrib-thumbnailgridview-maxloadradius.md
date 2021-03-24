---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt das Komponentenvorladeverhalten an. </p> <p>Bei Festlegung auf <span class="codeph"> -1</span> werden die Miniaturansichten gleichzeitig geladen, wenn die Komponente initialisiert wird oder sich das Asset ändert. </p> <p>Bei Festlegung auf <span class="codeph"> 0</span> werden nur die sichtbaren Miniaturansichten geladen. </p> <p>Legt <span class="codeph"><span class="varname"> preloadnbr</span></span> fest, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a3abd04c03e14c238a07349ce50d8310}

Optional.

## Standard {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Beispiel {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
