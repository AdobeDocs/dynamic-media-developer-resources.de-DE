---
title: ThumbnailGridView.maxLoadRadius
description: ThumbnailGridView.maxLoadRadius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
TQID: 'https://experienceleague.adobe.com/dbcZzhrzwZU5T307jcD6H6kx5RNeYWRBe21nD-2deXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 5%

---

# ThumbnailGridView.maxLoadRadius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

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

`1`

## Beispiel {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`

