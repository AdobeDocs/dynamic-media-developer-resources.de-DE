---
description: FavoritesView.maxLoadRadius
solution: Experience Manager
title: FavoritesView.maxLoadRadius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 440f147e-865c-4615-8d83-ea6431271612
TQID: 'https://experienceleague.adobe.com/Y6Yv-DLzkKMZMsiuZEPqdyTRpsMzqol4Lt8QTCTyVNs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 5%

---

# FavoritesView.maxLoadRadius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Bei <span class="codeph"> -1</span> werden alle Miniaturen gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Bei <span class="codeph"> 0</span> werden nur sichtbare Miniaturansichten geladen. </p> <p> Bei Festlegung auf <span class="codeph"><span class="varname"> preloadnbr</span></span> können Sie festlegen, wie viele unsichtbare Zeilen um den sichtbaren Bereich vorab geladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`]

