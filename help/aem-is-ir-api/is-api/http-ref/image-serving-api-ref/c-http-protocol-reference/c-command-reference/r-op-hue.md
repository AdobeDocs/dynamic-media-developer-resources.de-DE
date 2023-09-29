---
title: op_hue
description: Passt den Bildton an. Verschiebt die Farbtiefe jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes um den angegebenen Wert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# op_hue{#op-hue}

Passt den Bildton an. Verschiebt die Farbtiefe jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes um den angegebenen Wert.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Farbkorrektur in Grad (-180...+180 int). </p></td> 
 </tr> 
</table>

Basierend auf einem 360-Grad-Farbbereich.

## Eigenschaften {#section-55779644700b4c808a624cdf5a04447e}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp`. Wird von Effektebenen ignoriert. CMYK-Bilder oder -Ebenen werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Standard {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, ohne Änderung der Farbtiefe.
