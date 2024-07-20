---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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
   <td colname="col2"> <p> Steuert die Empfindlichkeit der horizontalen und vertikalen Rotation, die durch Ziehen oder Wischen mit der Maus durchgeführt wird. </p> <p> <span class="codeph"> xSensitivity</span> legt fest, wie viele horizontale Produktdrehungen durchgeführt werden, wenn der Benutzer die Maus horizontal von einer Seite der Ansicht zur anderen bewegt. Beispielsweise bedeutet drei, dass der Benutzer drei vollständige Rotations für eine volle Ziehen-Geste sieht. </p> <p>Genauso steuert <span class="codeph"> ySensitivity</span> die Empfindlichkeit der vertikalen Rotation. Der Wert 1 bedeutet, dass der Blickwinkel von der obersten Rotationsebene in die untere (oder umgekehrt) Ebene geändert wird. </p> <p>Wenn Sie einen negativen Wert für <span class="codeph"> ySensitivity</span> festlegen, wird die Richtung der vertikalen Rotation umgekehrt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
