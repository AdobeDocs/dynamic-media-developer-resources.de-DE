---
title: op_Saturation
description: Sättigung anpassen. Ändert die Sättigung jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# op_Saturation{#op-saturation}

Sättigung anpassen. Ändert die Sättigung jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Adj</span> </p> </td> 
  <td class="stentry"> <p>Sättigungseinstellung (-100…+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` das Bild vollständig entsättigt.

## Eigenschaften {#section-9a3cc9ff060049449554dfa69d92fd53}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, für keine Änderung der Sättigung. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Beispiel {#section-033b272f1b7e4efeb94e841fd8095357}

Bearbeiten Sie ein Farbfoto, um ein „hochwertiges“ Erscheinungsbild zu erzielen:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
