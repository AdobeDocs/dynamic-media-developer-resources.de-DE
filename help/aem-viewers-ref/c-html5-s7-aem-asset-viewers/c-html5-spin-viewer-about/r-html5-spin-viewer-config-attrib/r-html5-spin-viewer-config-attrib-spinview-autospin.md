---
description: 'null'
seo-description: 'null'
seo-title: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
topic: Dynamic media
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`durationdirectionspin_number`*][, *``*][, *``*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert oder deaktiviert die automatische Rotationsanimation. Um eine optimale automatische Rotation zu erzielen, wird empfohlen, alle Frames im Voraus zu laden, indem <span class="codeph"> maxloadradius</span> auf <span class="codeph"> -1</span>eingestellt wird. Beachten Sie jedoch, dass dies zu einer höheren Ladezeit und einer höheren Bandbreitennutzung führt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Die Anzahl der Sekunden pro Vollspin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Richtung</span></span> </p> </td> 
   <td colname="col2"> <p> Die Rotationsrichtung, die <span class="codeph"> 0</span> für die Spinnerei nach Osten und <span class="codeph"> 1</span> für die Spinnerei nach Westen ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Die Anzahl der vollständigen Drehungen, die vor dem Anhalten der automatischen Eingabe durchgeführt wurden. Die Zahl ist eine Gleitkommazahl. Für eine unendliche automatische Drehung auf <span class="codeph"> -1</span> eingestellt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
