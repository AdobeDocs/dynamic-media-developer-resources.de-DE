---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 440f147e-865c-4615-8d83-ea6431271612
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Wenn der Wert auf <span class="codeph"> -1</span> festgelegt ist, werden alle Miniaturansichten gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, werden nur sichtbare Miniaturansichten geladen. </p> <p> Wenn der Wert auf <span class="codeph"><span class="varname"> preloadnbr</span></span> festgelegt ist, können Sie festlegen, wie viele unsichtbare Zeilen um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`]
