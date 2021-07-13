---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# CallToAction.direction{#calltoaction-direction}

Konfigurationsattribut für interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie Miniaturansichten in der Ansicht gefüllt werden. </p> <p>Legen Sie <span class="codeph"> links </span> fest, um die Füllreihenfolge von links nach rechts festzulegen. </p> <p>Wird auf <span class="codeph"> rechts </span> gesetzt, wird die Reihenfolge umgekehrt, sodass die Ansicht von rechts nach links in Richtung von oben nach unten gefüllt wird. </p> <p>Legen Sie <span class="codeph"> auto </span> fest, damit die Komponente den richtigen Modus anwenden kann, wenn das Gebietsschema auf <span class="codeph"> "ja" </span> festgelegt ist; Andernfalls wird <span class="codeph"> left </span> verwendet. </p> </td> 
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
