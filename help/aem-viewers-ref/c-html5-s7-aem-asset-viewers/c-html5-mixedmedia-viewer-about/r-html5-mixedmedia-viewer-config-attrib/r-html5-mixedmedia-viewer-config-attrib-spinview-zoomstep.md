---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
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

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
