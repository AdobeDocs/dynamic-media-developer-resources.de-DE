---
description: Bildanker (Hotspot). Gibt den Texturankerpunkt (Hotspot) der wiederholbaren Textur oder des Dekormaterials an.
seo-description: Bildanker (Hotspot). Gibt den Texturankerpunkt (Hotspot) der wiederholbaren Textur oder des Dekormaterials an.
seo-title: anchor
solution: Experience Manager
title: Anker
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# anchor{#anchor}

Bildanker (Hotspot). Gibt den Texturankerpunkt (Hotspot) der wiederholbaren Textur oder des Dekormaterials an.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke des Quellbilds (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Offset vom Mittelpunkt des Quellbilds (real, real). </p></td> 
 </tr> 
</table>

Auf ein Vignettenobjekt wird eine wiederholbare Textur angewendet, sodass sich der Textur-Verankerungspunkt ( `anchor=`) am Texturpunkt des Objekts befindet.

Auf ein Vignettenobjekt wird ein Dezimalbild angewendet, sodass sich der dekale Verankerungspunkt am Dezimalpunkt des Objekts befindet. Die dekale Position kann mit dem Befehl `pos=` weiter angepasst werden.

`anchorN=0,0` platziert den Bildanker in der Mitte des Quellbilds. `anchorN=-0.5,-0.5` oder  `anchor=0,0` befindet sich in der oberen linken Ecke und  `anchorN=0.5,0.5` befindet sich in der unteren rechten Ecke des Quellbilds.

## Eigenschaften {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Materialattribut**. Wird ignoriert, wenn `align=2`, oder wenn das Material keine wiederholbare Textur, ein Hintergrund oder ein Dekorativ ist.

## Standard {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, wenn das Material auf einem Katalogeintrag basiert. Andernfalls `anchor=0,0` (die obere linke Ecke des Bilds) für wiederholbare Texturen und Hintergrundbilder und `anchorN=0,0` (die Mitte des Bilds) für Dezimalstellen.

## Verwandte Themen {#section-b18bf0b035644ca5aedebbc64373718e}

[Katalog::Anker](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
