---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duration`*][, *`Richtung`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert oder deaktiviert die automatische Rotation. Um das beste automatische Rotations-Erlebnis zu erzielen, wird empfohlen, alle Frames vorab zu laden, indem Sie <span class="codeph"> maxloadradius</span> nach <span class="codeph"> -1</span>. Beachten Sie jedoch, dass diese Einstellung zu erhöhter Ladezeit und höherer Bandbreitennutzung führt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Die Anzahl der Sekunden pro vollständiger Drehung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Richtung</span></span> </p> </td> 
   <td colname="col2"> <p> Die Rotationsrichtung, die <span class="codeph"> 0</span> für die Spinnerei nach Osten und <span class="codeph"> 1</span> für die Spinnerei nach Westen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Die Anzahl der vollständigen Rotationen, die vor dem Anhalten des Autospins durchgeführt wurden. Die Zahl ist eine Gleitkommazahl. Legen Sie fest auf <span class="codeph"> -1</span> für eine unendliche automatische Rotation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
