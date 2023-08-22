---
title: origin
description: Ebenenursprung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# origin{#origin}

Ebenenursprung.

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p></td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke der Ebene rect (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Versatz vom Mittelpunkt der Ebene rect (real, real). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Der Ebenenrect umfasst immer jede Änderung durch `extend=`.

Definiert den Ausrichtungspunkt des Ebenenrechtecks, mit dem das Ebenenrechteck relativ zu Ebene 0 über positioniert wird `pos=`. `originN=0,0` Positioniert den Ebenenursprung in der Mitte des Ebenenrechtecks. `originN=-0.5,-0.5` und `origin=0,0` oben links und `originN=0.5,0.5` ist die untere rechte Ecke des Ebenenrechtecks.

## Eigenschaften {#section-60f639e36ada43d1abc6bfc100afc925}

Ebenenattribut. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Ebenentransformationen ( `crop=`, `scale=`, `rotate=`, `flip=`) auf die Ebenenquelle angewendet. Überschreibungen `anchor=`. Wird von Effektebenen ignoriert.

## Standard {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Wenn `origin=` nicht angegeben ist, wird der Ebenenursprung durch Anwenden der Ebene auf den Bildanker bestimmt. Wenn der Bildanker nicht bekannt ist, wird die Mitte des Ebenenrechtecks ( `originN=0,0`) verwendet wird.

## Beispiel {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [expand=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
