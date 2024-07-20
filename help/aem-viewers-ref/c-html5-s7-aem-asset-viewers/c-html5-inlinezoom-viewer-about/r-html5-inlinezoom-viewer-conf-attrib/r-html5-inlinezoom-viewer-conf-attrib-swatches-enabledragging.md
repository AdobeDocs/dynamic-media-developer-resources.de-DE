---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

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

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
