---
description: Passen Sie die Helligkeit an. Verringert oder erhöht die Bildhelligkeit.
seo-description: Passen Sie die Helligkeit an. Verringert oder erhöht die Bildhelligkeit.
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---


# op_brightness{#op-brightness}

Passen Sie die Helligkeit an. Verringert oder erhöht die Bildhelligkeit.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Helligkeitsanpassung (-100...+100 int). </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`. Von Effektebenen ignoriert. CMYK-Bilder oder -Ebenen werden vor dem Anwenden des Vorgangs in RGB konvertiert.

## Standard {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, um keine Änderung der Helligkeit.

## Beispiel {#section-c25f952f1b77409abb9ccf885862d75c}

Darken Sie den Hintergrund eines Bilds leicht, um den Inhalt des Vordergrunds hervorzuheben:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
