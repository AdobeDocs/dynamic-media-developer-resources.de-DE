---
description: Renderausrichtung der Textur. Gibt an, welche der vom ausgewählten Vignettenobjekt definierten Herkünfte verwendet werden sollen.
seo-description: Renderausrichtung der Textur. Gibt an, welche der vom ausgewählten Vignettenobjekt definierten Herkünfte verwendet werden sollen.
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 4%

---


# align{#align}

Renderausrichtung der Textur. Gibt an, welche der vom ausgewählten Vignettenobjekt definierten Herkünfte verwendet werden sollen.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Standardmäßige (zentrierte) Herkunft. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Herkunft für kontinuierliche Übereinstimmung </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Ausrichtung nach dem Zufallsprinzip. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>Benutzerdefinierte Herkunft. </p></td> 
 </tr> 
</table>

Der Renderer wendet die Textur auf das Objekt an, sodass der Texturankerpunkt ( `anchor=`) mit dem angegebenen Herkunft-Punkt übereinstimmt.

Jedes Objekt kann bis zu 6 Herkünfte (0,1, 3, 4, 5, 6) definieren. Wenn ein `align`-Wert angegeben ist, der entsprechende Herkunft jedoch nicht vom Vignettenobjekt definiert ist, wird der Standardpunkt (Mitte-Übereinstimmung) für die Herkunft verwendet.

`align=2` gibt eine zufällige Texturausrichtung an. In diesem Fall  `anchor=` wird diese effektiv ignoriert.

Meist für Polstermaterialien, möglicherweise für Bekleidungsstoffe, verwendet, um die Ausrichtung der Textur zwischen benachbarten Objekten zu steuern.

## Eigenschaften {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materialattribut. Wird ignoriert, wenn ein Rahmen-Objekt für Wand-, Schrank-, Geräte- oder Fensterbezüge ausgewählt ist oder wenn das Material keine wiederholbare Textur ist.

## Standard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, wenn das Material auf einem Katalogeintrag basiert, andernfalls 0 (zentriert).

## Verwandte Themen {#section-945d1ce275df487d9d564d4043156c79}

[Katalog::Ausrichtung](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [Anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
