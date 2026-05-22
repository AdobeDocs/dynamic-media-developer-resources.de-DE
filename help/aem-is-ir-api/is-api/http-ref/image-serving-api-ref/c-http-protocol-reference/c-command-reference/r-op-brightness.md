---
title: op_bright
description: Helligkeit anpassen. Verringert oder erhöht die Bildhelligkeit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
TQID: 'https://experienceleague.adobe.com/EnNWm3aANmraWtDlmiz35cR8T9f5YjXuUdSM-E1gHAA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
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

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`. Von Effektebenen ignoriert. CMYK-Bilder oder -Ebenen werden in RGB konvertiert, bevor der Vorgang angewendet wird.

## Standard {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, für keine Helligkeitsänderung.

## Beispiel {#section-c25f952f1b77409abb9ccf885862d75c}

Dunkeln Sie den Hintergrund eines Bildes etwas ab, um den Vordergrundinhalt hervorzuheben:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
