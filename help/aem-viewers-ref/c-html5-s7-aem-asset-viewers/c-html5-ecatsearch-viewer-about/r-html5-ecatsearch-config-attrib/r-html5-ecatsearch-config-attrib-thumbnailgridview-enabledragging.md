---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Aktiviert oder deaktiviert die Möglichkeit für einen Benutzer, mit der Maus oder durch Berührungsgesten zu scrollen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funktionen innerhalb des Bereichs <span class="codeph"> 0-1 </span>. Dies ist ein <span class="codeph"> % </span> -Wert für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn er auf <span class="codeph"> 1 </span> gesetzt ist, bewegt er sich mit der Maus. Wenn es auf <span class="codeph"> 0 </span> gesetzt ist, lässt es Sie sich überhaupt nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-831c23dea82449bfa50fd155bea365b7}

Optional.

## Standard {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## Beispiel {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
