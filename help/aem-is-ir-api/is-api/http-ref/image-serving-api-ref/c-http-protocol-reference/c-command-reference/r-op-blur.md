---
description: Weichzeichnen des Bildes. Wendet einen Weichzeichnungsfilter auf die Bilddaten an.
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

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

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`.

## Standard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, um keinen Weichzeichnungseffekt zu erzielen.

## Beispiel {#section-1ebacde68388492eb108ae0fcd7424db}

Weichzeichnen des Hintergrunds eines Bildes Ein separates Maskenbild wird von `catalog::MaskPath` referenziert. Beachten Sie, dass `layer=0`explizit angegeben werden muss. Andernfalls wird `op_blur` auf das gesamte Composite-Bild angewendet.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
