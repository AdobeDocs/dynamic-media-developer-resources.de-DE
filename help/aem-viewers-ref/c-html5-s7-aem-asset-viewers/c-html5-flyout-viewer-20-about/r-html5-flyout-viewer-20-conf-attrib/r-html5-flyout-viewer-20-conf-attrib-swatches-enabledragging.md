---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
uuid: 2b5dff77-25e3-42cd-bdae-0a96f04f881e
feature: Dynamic Media Classic, Viewer, SDK/API, Flyout
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Aktiviert bzw. deaktiviert die Möglichkeit, dass ein Benutzer die Muster mit einer Maus oder mit Berührungsgesten durchblättert </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funktionen im Bereich <span class="codeph"> 0-1 </span>. Es handelt sich um einen <span class="codeph"> % </span>-Wert für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn sie auf <span class="codeph"> 1 </span> eingestellt ist, wird sie mit der Maus verschoben. Wenn sie auf <span class="codeph"> 0 </span> eingestellt ist, können Sie sich nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
