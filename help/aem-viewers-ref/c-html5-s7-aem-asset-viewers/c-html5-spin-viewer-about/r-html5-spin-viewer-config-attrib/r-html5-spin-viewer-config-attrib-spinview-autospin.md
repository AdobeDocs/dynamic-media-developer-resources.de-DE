---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duration`*][, *`direction`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert oder deaktiviert die automatische Rotationsanimation. Um ein optimales automatisches Rotations-Erlebnis zu erzielen, sollten Sie alle Frames vorab laden, indem Sie <span class="codeph"> maxLoadRadius</span> auf <span class="codeph"> -1</span> setzen. Beachten Sie jedoch, dass diese Einstellung zu einer verlängerten Ladezeit und einer höheren Bandbreitennutzung führt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Die Anzahl der Sekunden pro vollständigem Spin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Richtung</span></span> </p> </td> 
   <td colname="col2"> <p> Die Drehrichtung, die <span class="codeph"> 0</span> für die Drehung nach Osten und <span class="codeph"> 1</span> für die Drehung nach Westen beträgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Die Anzahl der vollständigen Rotationen, die durchgeführt wurden, bevor das automatische Drehen gestoppt wurde. Die Zahl ist eine Gleitkommazahl. Auf <span class="codeph"> -1</span> für einen unendlichen automatischen Spin eingestellt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
