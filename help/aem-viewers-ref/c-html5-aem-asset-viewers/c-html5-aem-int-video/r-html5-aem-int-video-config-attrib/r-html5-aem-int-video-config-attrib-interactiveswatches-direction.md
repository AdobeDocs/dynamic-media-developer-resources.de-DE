---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: InteractiveSwatches.directing
solution: Experience Manager
title: InteractiveSwatches.directing
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.directing{#interactiveswatches-direction}

Konfigurationsattribut für den interaktiven Video-Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie Muster in der Ansicht gefüllt werden. </p> <p>Auf <span class="codeph"> links einstellen, </span> um die Füllreihenfolge von links nach rechts festzulegen. </p> <p>Bei Auswahl von " <span class="codeph"> rechts"wird die Reihenfolge </span> umgekehrt, sodass die Ansicht von rechts nach links von oben nach unten gefüllt wird. </p> <p>Wenn <span class="codeph"> auto festgelegt </span> ist, wendet die Komponente den Modus right an, wenn das Gebietsschema auf <span class="codeph"> ja </span>"eingestellt ist. Andernfalls wird <span class="codeph"> links </span> verwendet. </p> </td> 
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

