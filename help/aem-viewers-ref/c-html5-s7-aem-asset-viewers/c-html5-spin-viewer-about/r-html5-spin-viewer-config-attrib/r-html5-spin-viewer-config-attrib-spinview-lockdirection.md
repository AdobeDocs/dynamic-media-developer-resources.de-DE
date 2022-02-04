---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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
   <td colname="col2"> <p> Gibt an, ob eine Änderung der Rotationsrichtung zulässig ist, wenn ein 2D-Rotationsset vorhanden ist. </p> <p>Wenn auf <span class="codeph"> 1 </span>, identifiziert die Komponente die primäre Drag- oder Wischrichtung (horizontal oder vertikal) am Anfang der Geste. Danach bleibt diese Richtung erhalten, bis die Geste endet. Wenn der Benutzer z. B. eine horizontale Rotation beginnt und dann beschließt, seine Ziehen-Geste in vertikaler Richtung fortzusetzen, führt die Komponente keine vertikale Rotation durch. Stattdessen wird nur die horizontale Bewegung der Maus oder des Wischens berücksichtigt. </p> <p>Ein Wert von <span class="codeph"> 0 </span> ermöglicht dem Benutzer, die Rotationsrichtung während des Gestenfortschritts jederzeit zu ändern. Die Einstellung hat keine Auswirkung, wenn das Rotationsset 1D ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
