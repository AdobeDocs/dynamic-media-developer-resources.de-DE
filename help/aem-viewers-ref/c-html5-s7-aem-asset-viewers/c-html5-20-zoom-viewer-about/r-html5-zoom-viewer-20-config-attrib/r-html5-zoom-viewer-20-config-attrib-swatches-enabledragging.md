---
description: 'null'
seo-description: 'null'
seo-title: Muster.Ziehen aktivieren
solution: Experience Manager
title: Muster.Ziehen aktivieren
topic: Dynamic media
uuid: 0bfd7275-59c7-446f-b056-93ed79352462
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Muster.Ziehen aktivieren{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Aktiviert bzw. deaktiviert die Möglichkeit, dass ein Benutzer die Muster mit einer Maus oder mit Berührungsgesten durchblättert </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td> <p> Funktionen innerhalb des <span class="codeph"> Bereichs 0-1 </span> . Es handelt sich um einen <span class="codeph"> Wert von </span> % für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. Wenn es auf <span class="codeph"> 1 eingestellt ist, </span>bewegt es sich mit der Maus. Wenn sie auf <span class="codeph"> 0 gesetzt ist, </span>lässt sie Sie überhaupt nicht in die falsche Richtung. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
