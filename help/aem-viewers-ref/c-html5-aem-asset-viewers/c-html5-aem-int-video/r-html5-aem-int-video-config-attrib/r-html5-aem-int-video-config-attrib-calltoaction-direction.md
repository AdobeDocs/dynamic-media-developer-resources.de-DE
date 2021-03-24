---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
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

