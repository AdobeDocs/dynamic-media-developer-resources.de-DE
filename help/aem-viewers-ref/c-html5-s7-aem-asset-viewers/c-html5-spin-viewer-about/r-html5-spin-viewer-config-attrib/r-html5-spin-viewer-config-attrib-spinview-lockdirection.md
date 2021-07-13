---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Viewer,SDK/API,Rotationssets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, ob bei 2D-Rotationsset eine Änderung der Rotationsrichtung zulässig ist. </p> <p>Wenn der Wert auf <span class="codeph"> 1 </span> festgelegt ist, gibt die Komponente die primäre Drag- oder Wischrichtung (horizontal oder vertikal) am Anfang der Geste an. Danach bleibt diese Richtung erhalten, bis die Geste endet. Wenn der Benutzer z. B. eine horizontale Rotation beginnt und dann beschließt, seine Ziehen-Geste in vertikaler Richtung fortzusetzen, führt die Komponente keine vertikale Rotation durch. Stattdessen wird nur die horizontale Bewegung der Maus oder des Wischens berücksichtigt. </p> <p>Mit dem Wert <span class="codeph"> 0 </span> kann ein Benutzer die Rotationsrichtung während des Gestenfortschritts jederzeit ändern. Die Einstellung hat keine Auswirkungen, wenn das Rotationsset 1D ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
