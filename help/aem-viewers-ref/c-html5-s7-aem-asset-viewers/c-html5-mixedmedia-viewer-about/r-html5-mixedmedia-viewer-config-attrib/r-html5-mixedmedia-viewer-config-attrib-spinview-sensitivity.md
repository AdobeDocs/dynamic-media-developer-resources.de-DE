---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

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
