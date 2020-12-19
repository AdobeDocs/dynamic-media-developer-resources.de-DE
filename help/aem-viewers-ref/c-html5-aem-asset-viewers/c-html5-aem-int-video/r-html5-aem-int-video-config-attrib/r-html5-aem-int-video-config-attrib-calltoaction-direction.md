---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: CallToAction.direction
solution: Experience Manager
title: CallToAction.direction
topic: Dynamic media
uuid: fe182e8f-696d-4515-afdb-49964a374dae
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---


# CallToAction.direction{#calltoaction-direction}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie Miniaturansichten in der Ansicht gefüllt werden. </p> <p>Auf <span class="codeph"> links </span> setzen, um die Füllreihenfolge von links nach rechts festzulegen. </p> <p>Bei Auswahl von <span class="codeph"> rechts </span> wird die Reihenfolge umgekehrt, sodass die Ansicht von oben nach unten in der rechten Richtung gefüllt wird. </p> <p>Auf <span class="codeph"> auto </span> setzen, damit die Komponente den rechten Modus anwenden kann, wenn das Gebietsschema auf <span class="codeph"> "ja" </span> eingestellt ist; Andernfalls wird <span class="codeph"> links </span> verwendet. </p> </td> 
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

