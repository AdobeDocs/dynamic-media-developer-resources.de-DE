---
title: InteractiveSwatches.direction
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Konfigurationsattribut für interaktiven Video-Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie Muster in der Ansicht gefüllt werden. </p> <p>Legen Sie <span class="codeph"> links </span> fest, um die Füllreihenfolge von links nach rechts festzulegen. </p> <p>Wird auf <span class="codeph"> rechts </span> gesetzt, wird die Reihenfolge umgekehrt, sodass die Ansicht von rechts nach links in Richtung von oben nach unten gefüllt wird. </p> <p>Wenn <span class="codeph"> auto </span> festgelegt ist, wendet die Komponente den richtigen Modus an, wenn das Gebietsschema auf " <span class="codeph"> ja </span>"festgelegt ist. Andernfalls wird <span class="codeph"> left </span> verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
