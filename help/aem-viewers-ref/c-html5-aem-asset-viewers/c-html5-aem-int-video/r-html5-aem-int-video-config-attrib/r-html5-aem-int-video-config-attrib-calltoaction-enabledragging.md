---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
topic: Dynamic media
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Aktiviert bzw. deaktiviert die Möglichkeit, mit einer Maus oder mit Touch-Gesten durch die Miniaturansichten zu blättern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td colname="col2"> <p> Liegt im <span class="codeph"> Bereich 0-1 </span> und ist ein Prozentwert für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. </p> <p>Wenn auf <span class="codeph"> 1 gesetzt, bewegt </span> es sich mit der Maus. </p> <p>Bei einem Wert von <span class="codeph"> 0 können Sie </span> sich nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

