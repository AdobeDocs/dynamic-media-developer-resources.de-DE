---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: acbcea10-950d-4f98-be5a-5aead9f4e0d9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadNbr</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Bei <span class="codeph"> -1 </span> die Miniaturen gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Bei Einstellung auf <span class="codeph"> 0 </span> nur die sichtbaren Miniaturansichten geladen. </p> <p>set <span class="codeph"><span class="varname"> preloadnbr</span></span> legt fest, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a3abd04c03e14c238a07349ce50d8310}

Optional.

## Standard {#section-c60e81667965460cbf03378a1ab9b187}

[!DNL `1`]

## Beispiel {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
