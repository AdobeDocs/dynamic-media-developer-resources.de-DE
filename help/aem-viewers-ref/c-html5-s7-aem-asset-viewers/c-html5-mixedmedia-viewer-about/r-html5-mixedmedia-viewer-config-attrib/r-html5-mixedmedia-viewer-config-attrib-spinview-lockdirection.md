---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 2%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, ob eine Änderung der Drehrichtung zulässig ist, wenn ein 2D-Rotationsset vorhanden ist. </p> <p>Bei <span class="codeph"> 1 </span> identifiziert die Komponente die primäre Ziehen- oder Wischrichtung (horizontal versus vertikal) zu Beginn der Geste. Danach behält sie diese Richtung bei, bis die Geste beendet ist. Wenn der/die Benutzende beispielsweise eine horizontale Drehung startet und dann beschließt, seine/ihre Ziehgeste in vertikaler Richtung fortzusetzen, führt die Komponente keine vertikale Drehung durch. Stattdessen wird nur die horizontale Bewegung der Maus oder das Wischen berücksichtigt. </p> <p>Mit einem Wert von <span class="codeph"> 0 </span> können Benutzende die Drehrichtung jederzeit während des Gestenfortschritts ändern. Die Einstellung hat keine Auswirkung, wenn das Rotationsset 1D ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
