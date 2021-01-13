---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, ob im Falle eines 2D-Rotationssets eine Änderung der Rotationsrichtung zulässig ist. </p> <p>Bei Festlegung auf <span class="codeph"> 1 </span> gibt die Komponente die primäre Drag- oder Blätterrichtung (horizontal oder vertikal) am Beginn der Geste an. Danach bleibt die Richtung erhalten, bis die Geste endet. Wenn der Benutzer beispielsweise eine horizontale Drehung Beginn und dann beschließt, die Ziehbewegung in vertikaler Richtung fortzusetzen, führt die Komponente keine vertikale Drehung durch; sondern nur die horizontale Bewegung der Maus oder des Wischens. </p> <p>Mit dem Wert <span class="codeph"> 0 </span> kann ein Benutzer die Rotationsrichtung während des Gestenfortschritts jederzeit ändern. Die Einstellung hat keine Auswirkung, wenn das Rotationsset 1D ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
