---
title: op_sättigung
description: Sättigung anpassen. Ändert die Sättigung jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---

# op_sättigung{#op-saturation}

Sättigung anpassen. Ändert die Sättigung jedes sichtbaren Pixels der Ebene oder des zusammengesetzten Bildes.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Sättigungsanpassung (-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` entfernt das Bild vollständig.

## Eigenschaften {#section-9a3cc9ff060049449554dfa69d92fd53}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp`. Wird von Effektebenen ignoriert.

## Standard {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, um keine Sättigung zu ändern. CMYK-Bilder oder -Ebenen werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Beispiel {#section-033b272f1b7e4efeb94e841fd8095357}

Bearbeiten Sie ein Farbfoto, um ein &quot;High-Key&quot;-Erscheinungsbild zu erhalten:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
