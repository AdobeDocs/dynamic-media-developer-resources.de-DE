---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Aktiviert oder deaktiviert das Scrollen der Farbfelder mit der Maus oder mithilfe von Touch-Gesten </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funktioniert im <span class="codeph"> 0-1 </span>. Es handelt sich um einen <span class="codeph"> von </span> % für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn er auf <span class="codeph"> 1 </span> eingestellt ist, bewegt er sich mit der Maus. Wenn sie auf <span class="codeph"> 0 </span> eingestellt ist, können Sie sich überhaupt nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-831c23dea82449bfa50fd155bea365b7}

Optional.

## Standard {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Beispiel {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
