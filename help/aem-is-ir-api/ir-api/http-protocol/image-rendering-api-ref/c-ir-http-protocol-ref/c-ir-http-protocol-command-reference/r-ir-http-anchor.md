---
title: anchor
description: Bildanker (Hotspot). Gibt den Textur-Ankerpunkt (Hotspot) des wiederholbaren Textur- oder Abziehmaterials an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
TQID: 'https://experienceleague.adobe.com/fw1-eDsdT8jsgJfXBzb2bsLlcuTxKdLUmIeD5cFDiFE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
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
