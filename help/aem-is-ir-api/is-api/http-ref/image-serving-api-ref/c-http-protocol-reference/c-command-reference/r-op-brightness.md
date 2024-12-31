---
title: op_bright
description: Helligkeit anpassen. Verringert oder erhöht die Bildhelligkeit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_bright{#op-brightness}

Helligkeit anpassen. Verringert oder erhöht die Bildhelligkeit.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Adj</span> </p> </td> 
  <td class="stentry"> <p>Helligkeitseinstellung (-100…+100 int). </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Standard {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, für keine Helligkeitsänderung.

## Beispiel {#section-c25f952f1b77409abb9ccf885862d75c}

Dunkeln Sie den Hintergrund eines Bildes etwas ab, um den Vordergrundinhalt hervorzuheben:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
