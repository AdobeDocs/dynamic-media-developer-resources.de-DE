---
title: CallToAction.direction
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

Konfigurationsattribut für interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie Miniaturansichten in der Ansicht gefüllt werden. </p> <p>Setzen Sie dies auf <span class="codeph"> left </span> , um die Füllreihenfolge von links nach rechts festzulegen. </p> <p>Wird auf <span class="codeph"> rechts </span> gesetzt, wird die Reihenfolge umgekehrt, sodass die Ansicht von rechts nach links von oben nach unten gefüllt wird. </p> <p>Auf <span class="codeph"> auto </span> setzen, damit die Komponente den rechten Modus anwendet, wenn das Gebietsschema auf <span class="codeph"> "ja" </span> festgelegt ist; andernfalls wird <span class="codeph"> left </span> verwendet. </p> </td> 
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
