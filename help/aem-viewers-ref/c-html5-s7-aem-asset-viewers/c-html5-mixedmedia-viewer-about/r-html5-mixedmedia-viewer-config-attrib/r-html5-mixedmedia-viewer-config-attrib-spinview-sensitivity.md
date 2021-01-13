---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 7c63a7c5-ac75-485d-94ac-d1e133fbe44f
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitätSensitivität`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Steuert die Empfindlichkeit der horizontalen und vertikalen Rotation, die mit einem Mausziehen oder Wischen ausgeführt wird. </p> <p> <span class="codeph"> Legt </span> xSensitivityfest, wie viele vollständige horizontale Produktdrehungen durchgeführt werden, wenn der Benutzer die Maus horizontal von einer Seite der Ansicht zur anderen bewegt. Beispielsweise bedeutet dies, dass dem Benutzer drei vollständige Rotationssets für eine volle Ziehgeste angezeigt werden. </p> <p>Gleichermaßen steuert <span class="codeph"> ySensitivity</span> die Empfindlichkeit der vertikalen Drehung. Der Wert 1 bedeutet, dass bei einem vollständigen vertikalen Ziehen oder Wischen der Winkel der Ansicht von der obersten Rotationsebene zur untersten Ebene (oder umgekehrt) geändert wird. </p> <p>Wenn Sie einen negativen Wert für <span class="codeph"> ySensitivity</span> festlegen, wird die Richtung der vertikalen Drehung umgekehrt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
