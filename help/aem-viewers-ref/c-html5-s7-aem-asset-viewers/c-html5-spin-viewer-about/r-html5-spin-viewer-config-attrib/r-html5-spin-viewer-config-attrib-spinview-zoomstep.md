---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Schritt</span></span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Anzahl der Aktionen zum Ein- und Auszoomen, die erforderlich sind, um die Auflösung um den Faktor zwei zu erhöhen oder zu verringern. Die Auflösungsänderung für jede Zoom-Aktion beträgt 2^1 pro Schritt. Auf <span class="codeph"> 0</span> eingestellt, um mit einer einzigen Zoom-Aktion auf die volle Auflösung zu zoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Limit</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die maximale Zoom-Auflösung relativ zum Bild mit voller Auflösung fest. Der Standardwert ist <span class="codeph"> 1.0</span>, wodurch das Zoomen über die volle Auflösung hinaus nicht möglich ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
