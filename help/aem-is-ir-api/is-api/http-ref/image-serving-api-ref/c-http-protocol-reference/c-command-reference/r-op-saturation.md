---
description: Passen Sie die Sättigung an. Ändert die Sättigung jedes sichtbaren Pixels der Ebene oder des Composite-Bildes.
solution: Experience Manager
title: op_Saturation
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# op_Saturation{#op-saturation}

Passen Sie die Sättigung an. Ändert die Sättigung jedes sichtbaren Pixels der Ebene oder des Composite-Bildes.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Sättigungsanpassung (-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` Sättigt die Sättigung des Bildes vollständig.

## Eigenschaften {#section-9a3cc9ff060049449554dfa69d92fd53}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, ohne dass sich die Sättigung ändert. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Beispiel {#section-033b272f1b7e4efeb94e841fd8095357}

Bearbeiten Sie ein Farbfoto, um ein &quot;high-key&quot;-Erscheinungsbild zu erzielen:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
