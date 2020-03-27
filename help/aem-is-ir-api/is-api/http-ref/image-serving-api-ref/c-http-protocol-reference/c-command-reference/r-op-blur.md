---
description: Weichzeichnen des Bildes. Wendet einen Weichzeichnungsfilter auf die Bilddaten an.
seo-description: Weichzeichnen des Bildes. Wendet einen Weichzeichnungsfilter auf die Bilddaten an.
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Scene7 Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_blur{#op-blur}

Weichzeichnen des Bildes. Wendet einen Weichzeichnungsfilter auf die Bilddaten an.

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Weichzeichnungsfilterradius in Pixel (real 0.100). </p></td> 
 </tr> 
</table>

*`radius`* in Pixeln relativ zum Composite-Bild. Ebenfalls zum Weichzeichnen von Ebeneneffekten verwendet.

## Eigenschaften {#section-92573fe2c07746a7bab93a81fc3d208d}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, falls `layer=comp`dies der Fall ist.

## Standard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, um keinen Weichzeichnungseffekt zu erzielen.

## Beispiel {#section-1ebacde68388492eb108ae0fcd7424db}

Weichzeichnen des Hintergrunds eines Bildes Auf ein anderes Maskenbild wird verwiesen `catalog::MaskPath`. Beachten Sie, dass dies explizit angegeben werden `layer=0`muss. Andernfalls `op_blur` wird das gesamte Composite-Bild angewendet.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
