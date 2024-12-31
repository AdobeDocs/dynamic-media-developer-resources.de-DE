---
title: op_blur
description: Bild unscharf machen. Wendet einen Weichzeichnungsfilter auf die Bilddaten an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

Bild unscharf machen. Wendet einen Weichzeichnungsfilter auf die Bilddaten an.

`op_blur= *`Radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Radius</span> </p> </td> 
  <td class="stentry"> <p>Weichzeichnungsfilterradius in Pixeln (real 0..100). </p></td> 
 </tr> 
</table>

*`radius`* ist in Pixeln relativ zum zusammengesetzten Bild. Wird auch verwendet, um Ebeneneffekte zu federn.

## Eigenschaften {#section-92573fe2c07746a7bab93a81fc3d208d}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`.

## Standard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, für keinen Weichzeichnungseffekt.

## Beispiel {#section-1ebacde68388492eb108ae0fcd7424db}

Blur den Hintergrund eines Bildes. Ein separates Maskenbild wird von `catalog::MaskPath` referenziert. Beachten Sie, dass `layer=0`explizit angegeben werden muss, da andernfalls `op_blur` auf das gesamte zusammengesetzte Bild angewendet werden würde.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
