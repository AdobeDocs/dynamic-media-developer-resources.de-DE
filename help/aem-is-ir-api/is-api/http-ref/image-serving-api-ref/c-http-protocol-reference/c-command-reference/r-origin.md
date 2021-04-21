---
description: Herkunft der Ebene.
solution: Experience Manager
title: Herkunft
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# Herkunft{#origin}

Herkunft der Ebene.

`origin= *`Kohle`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kohle</span> </p></td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke des Ebenenrects (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Offset vom Mittelpunkt des Ebenenrects (real, real). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Der Ebenenrect enthält immer alle Änderungen von `extend=`.

Definiert den Ausrichtungspunkt des Ebenenrechtecks, mit dem das Ebenenrechteck relativ zur Ebene 0 mithilfe von `pos=` positioniert wird. `originN=0,0` Positioniert die Herkunft der Ebene in der Mitte des Ebenenrechtecks. `originN=-0.5,-0.5` und  `origin=0,0` ist die obere linke Ecke und  `originN=0.5,0.5` die untere rechte Ecke des Ebenenrechtecks.

## Eigenschaften {#section-60f639e36ada43d1abc6bfc100afc925}

Ebenenattribut. Gilt für die aktuelle Ebene oder für Ebene 0, wenn `layer=comp`. Nicht betroffen von Ebenentransformationen ( `crop=`, `scale=`, `rotate=`, `flip=`), die auf die Ebenenquelle angewendet werden. Überschreibt `anchor=`. Von Effektebenen ignoriert.

## Standard {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Wenn `origin=` nicht angegeben ist, wird die Herkunft der Ebene bestimmt, indem die Ebene auf den Bildanker angewendet wird. Wenn der Bildanker nicht bekannt ist, wird die Mitte des Ebenenrechtecks ( `originN=0,0`) verwendet.

## Beispiel {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
