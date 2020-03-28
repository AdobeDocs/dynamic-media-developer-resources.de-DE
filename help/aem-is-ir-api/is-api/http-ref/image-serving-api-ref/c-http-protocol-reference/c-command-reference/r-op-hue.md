---
description: Passen Sie den Farbton an. Verschiebt den Farbton jedes sichtbaren Pixels der Ebene oder des Composite-Bildes um den angegebenen Wert.
seo-description: Passen Sie den Farbton an. Verschiebt den Farbton jedes sichtbaren Pixels der Ebene oder des Composite-Bildes um den angegebenen Wert.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Scene7 Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_hue{#op-hue}

Passen Sie den Farbton an. Verschiebt den Farbton jedes sichtbaren Pixels der Ebene oder des Composite-Bildes um den angegebenen Wert.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Farbtonanpassung in Grad (-180...+180 int). </p></td> 
 </tr> 
</table>

Basierend auf einem 360-Grad-Farbtonbereich.

## Eigenschaften {#section-55779644700b4c808a624cdf5a04447e}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, falls `layer=comp`dies der Fall ist. Von Effektebenen ignoriert. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Standard {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, ohne dass sich der Farbton ändert.
