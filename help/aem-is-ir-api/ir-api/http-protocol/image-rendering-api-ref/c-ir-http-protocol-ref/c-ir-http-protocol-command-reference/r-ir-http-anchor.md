---
title: anchor
description: Bildanker (Hotspot). Gibt den Textur-Ankerpunkt (Hotspot) des wiederholbaren Textur- oder Abziehmaterials an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# anchor{#anchor}

Bildanker (Hotspot). Gibt den Textur-Ankerpunkt (Hotspot) des wiederholbaren Textur- oder Abziehmaterials an.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Pixel-Offset von der linken oberen Ecke des Quellbilds (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> XN</span>, <span class="varname"> YN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Versatz von der Mitte des Quellbilds (real, real). </p></td> 
 </tr> 
</table>

Auf ein Vignettenobjekt wird eine wiederholbare Textur angewendet, sodass sich der Texturankerpunkt ( `anchor=`) am Texturursprungspunkt des Objekts befindet.

Ein Abziehbild wird auf ein Vignettenobjekt angewendet, sodass sich der Abziehbildankerpunkt am Abziehbildursprungspunkt des Objekts befindet. Die Abziehbildposition kann mit dem Befehl `pos=` weiter eingestellt werden.

`anchorN=0,0` Platziert den Bildanker in der Mitte des Quellbilds. `anchorN=-0.5,-0.5` oder `anchor=0,0` befindet sich in der oberen linken Ecke und `anchorN=0.5,0.5` in der unteren rechten Ecke des Quellbilds.

## Eigenschaften {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Materialattribut**. Wird ignoriert, wenn `align=2` oder wenn das Material keine wiederholbare Textur, keine Tapete oder kein Abziehbild ist.

## Standard {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, wenn das Material auf einem Katalogeintrag basiert. Andernfalls `anchor=0,0` (die obere linke Ecke des Bildes) für wiederholbare Texturen und Tapeten und `anchorN=0,0` (die Mitte des Bildes) für Abziehbilder.

## Verwandte Themen {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
