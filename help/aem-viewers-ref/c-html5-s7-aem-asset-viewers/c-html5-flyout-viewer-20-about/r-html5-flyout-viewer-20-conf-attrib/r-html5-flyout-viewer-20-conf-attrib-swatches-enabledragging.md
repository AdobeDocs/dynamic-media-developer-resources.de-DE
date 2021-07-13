---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Viewer,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Aktiviert oder deaktiviert die Möglichkeit für einen Benutzer, mit der Maus oder durch Berührungsgesten zu scrollen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funktionen innerhalb des Bereichs <span class="codeph"> 0-1 </span>. Es handelt sich um einen <span class="codeph"> % </span>-Wert für Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn er auf <span class="codeph"> 1 </span> gesetzt ist, bewegt er sich mit der Maus. Wenn es auf <span class="codeph"> 0 </span> gesetzt ist, können Sie sich nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
