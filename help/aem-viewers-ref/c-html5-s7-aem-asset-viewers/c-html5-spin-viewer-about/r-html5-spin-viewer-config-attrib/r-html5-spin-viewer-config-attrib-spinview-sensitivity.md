---
title: SpinView.sensitive
description: SpinView.sensitive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
TQID: 'https://experienceleague.adobe.com/B19x2Bn3GNq8YFUo-0HiSbyBQ4qrMcONvRSN1tNqOg0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# SpinView.sensitive{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Steuert die Empfindlichkeit der horizontalen und vertikalen Rotation, die mit einem Mausziehen oder Wischen durchgeführt wird. </p> <p> <span class="codeph"> xSensitivity</span> Legt fest, wie viele vollständige horizontale Produktrotationen vorgenommen werden, wenn Benutzende ihre Maus horizontal von einer Seite der Ansicht zur anderen ziehen. Beispielsweise bedeutet drei, dass der/die Benutzende drei vollständige Rotationen für eine vollständige Drag-Geste sieht. </p> <p>Ebenso steuert <span class="codeph"> ySensitivity</span> die Empfindlichkeit des vertikalen Spins. Der Wert 1 bedeutet, dass durch Ziehen oder Wischen der Ansichtswinkel von der obersten Ebene der Drallebene zur untersten Ebene (oder umgekehrt) geändert wird. </p> <p>Durch Festlegen eines negativen Werts für <span class="codeph"> ySensitivity</span> wird die Richtung des vertikalen Drehs umgekehrt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
