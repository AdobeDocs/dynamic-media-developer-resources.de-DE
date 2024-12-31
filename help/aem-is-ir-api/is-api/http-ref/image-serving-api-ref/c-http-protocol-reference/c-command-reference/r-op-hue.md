---
title: op_hue
description: Stellt den Bildton ein. Verschiebt den Farbton jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes um den angegebenen Betrag.
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

Stellt den Bildton ein. Verschiebt den Farbton jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes um den angegebenen Betrag.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Adj</span> </p> </td> 
  <td class="stentry"> <p>Farbtoneinstellung in Grad (-180…+180 int). </p></td> 
 </tr> 
</table>

Basierend auf einem Farbtonbereich von 360 Grad.

## Eigenschaften {#section-55779644700b4c808a624cdf5a04447e}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Standard {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, für keine Änderung des Farbtons.
