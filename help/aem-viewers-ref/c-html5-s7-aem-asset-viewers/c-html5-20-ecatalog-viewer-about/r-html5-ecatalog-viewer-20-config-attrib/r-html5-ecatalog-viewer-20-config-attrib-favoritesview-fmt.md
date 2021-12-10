---
title: FavoritesView.fmt
description: FavoritesView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 5%

---

# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Gibt das Bildformat an, das von der Komponente zum Laden von Bildern vom Image-Server verwendet wird. Das Format ist ein beliebiger Wert, der vom Image-Server und vom Client-Browser unterstützt wird. </p> <p>Wenn das Bildformat mit <span class="codeph"> -alpha</span>, rendert die Komponente die Bilder als transparenten Inhalt. Bei allen anderen Bildformatwerten behandelt die Komponente Bilder als deckend. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
