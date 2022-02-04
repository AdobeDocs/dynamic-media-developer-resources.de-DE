---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivität`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivität</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Steuert die Empfindlichkeit der horizontalen und vertikalen Rotation, die durch Ziehen oder Wischen mit der Maus durchgeführt wird. </p> <p> <span class="codeph"> xSensitivität</span> Legt fest, wie viele vollständige horizontale Produktdrehungen durchgeführt werden, wenn der Benutzer die Maus horizontal von einer Seite der Ansicht zur anderen bewegt. Beispielsweise bedeutet drei, dass der Benutzer drei vollständige Rotations für eine volle Ziehen-Geste sieht. </p> <p>Ebenso <span class="codeph"> ySensitivity</span> steuert die Empfindlichkeit der vertikalen Rotation. Der Wert 1 bedeutet, dass der Blickwinkel von der obersten Rotationsebene in die untere (oder umgekehrt) Ebene geändert wird. </p> <p>Festlegen eines negativen Werts für <span class="codeph"> ySensitivity</span> kehrt die Richtung der vertikalen Rotation um. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
