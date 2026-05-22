---
title: SpinView.zoomStep
description: SpinView.zoomStep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
TQID: 'https://experienceleague.adobe.com/QVBma1DuQ-dHIYvG-RE-eyf-PXyMgZv-MGYZIXrXbA4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# SpinView.zoomStep{#spinview-zoomstep}

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
