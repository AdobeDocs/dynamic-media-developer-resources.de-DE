---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Viewer,SDK/API,Rotationssets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span> [,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Steuert die Empfindlichkeit der horizontalen und vertikalen Rotation, die durch Ziehen oder Wischen mit der Maus durchgeführt wird. </p> <p> <span class="codeph"> </span> xSensitivitysets wie viele horizontale Produktdrehungen durchgeführt werden, wenn der Benutzer die Maus horizontal von einer Seite der Ansicht zur anderen bewegt. Beispielsweise bedeutet drei, dass der Benutzer drei vollständige Rotations für eine volle Ziehen-Geste sieht. </p> <p>Ebenso steuert <span class="codeph"> ySensitivity</span> die Empfindlichkeit der vertikalen Rotation. Der Wert 1 bedeutet, dass der Blickwinkel von der obersten Rotationsebene in die unterste Ebene (oder umgekehrt) geändert wird. </p> <p>Wenn Sie einen negativen Wert für <span class="codeph"> ySensitivity</span> festlegen, wird die Richtung der vertikalen Rotation umgekehrt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
