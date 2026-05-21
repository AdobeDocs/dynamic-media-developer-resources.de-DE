---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
TQID: 'https://experienceleague.adobe.com/ZQj4mwz-MZWHf8MeY-hrrESZLucBeqXpGQV6tnD-U9w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 5%

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
