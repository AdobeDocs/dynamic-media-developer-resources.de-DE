---
title: Ursprung
description: Ebenenursprung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5ea8eb18-d169-4255-b4b1-dda849246485
TQID: 'https://experienceleague.adobe.com/-wkJjmR-LwxC90IMLNXldXSiaugkaYRyvLS17-nbJAM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 2%

---

# Ursprung{#origin}

Ebenenursprung.

`origin= *`coord`*`

`originN= *`coordN`*`

<table id="simpletable_A270FD92B1E841FE81F5AB300351FE01"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Coord</span> </p></td> 
  <td class="stentry"> <p>Pixel-Versatz von der oberen linken Ecke des Ebenenrechts (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Normalisierter Versatz von der Mitte der Ebene rect (real, real). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>Der Layer React enthält immer alle Änderungen durch `extend=`.

Definiert den Ausrichtungspunkt des Ebenenrechtecks, der verwendet wird, um das Ebenenrechteck relativ zu Ebene 0 über `pos=` zu positionieren. `originN=0,0` Positioniert den Ebenenursprung in der Mitte des Ebenenrechtecks. `originN=-0.5,-0.5` und `origin=0,0` ist die obere linke Ecke und `originN=0.5,0.5` die untere rechte Ecke des Ebenenrechtecks.

## Eigenschaften {#section-60f639e36ada43d1abc6bfc100afc925}

Ebenenattribut. Gilt für die aktuelle Ebene oder, falls `layer=comp`, für Ebene 0. Nicht betroffen von Ebenentransformationen ( `crop=`, `scale=`, `rotate=`, `flip=`), die auf die Ebenenquelle angewendet wurden. Überschreibt `anchor=`. Von Effektebenen ignoriert.

## Standard {#section-b7209e5c2ad6491fb0c2353cc3f1f703}

Wenn `origin=` nicht angegeben ist, wird der Ebenenursprung bestimmt, indem die Ebenentransformationen auf den Bildanker angewendet werden. Wenn der Bildanker nicht bekannt ist, wird die Mitte des Ebenenrechtecks (`originN=0,0`) verwendet.

## Beispiel {#section-13e38d6e17be4e6cbc6b27fbde63b291}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-a9f9c42c86fe45798deb2daaf27ea5b7}

[Anker=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [Pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [Extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
