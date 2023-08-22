---
title: Zuschneiden
description: Bild beschneiden. Gibt einen rechteckigen Zuschnittbereich an, der entweder in Pixel ausgedrückt oder relativ zum Quellbild oder Maskenbild mit voller Auflösung normalisiert wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Zuschneiden{#crop}

Bild beschneiden. Gibt einen rechteckigen Zuschnittbereich an, der entweder in Pixel ausgedrückt oder relativ zum Quellbild oder Maskenbild mit voller Auflösung normalisiert wird.

`crop= *`coord`*, *`size`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Pixel-Versatz von der oberen linken Ecke des Quellbilds zur oberen linken Ecke des Zuschnittrects (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Normalisierter Versatz von der linken oberen Ecke des Quellbilds zur linken oberen Ecke des Zuschnittrects (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Größe der Zuschnittrect in Pixel (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Normalisierte Größe der Zuschnittgrafik relativ zur Größe des Quellbilds (real, real). </p></td> 
 </tr> 
</table>

Kann auch verwendet werden, um das Bild über seine Grenzen hinaus zu erweitern, indem negative x-, y-Werte und/oder Breite angegeben werden, Höhenwerte größer als die Bildbreite und -höhe. In diesem Fall ist der erweiterte Bereich vollständig transparent (sofern `bgColor=` angegeben ist).

## Eigenschaften {#section-632e0405bb9940679b5f8b1c10e0902e}

Quellbild-/Maskenattribut. Gilt für das Quellbild der Ebene 0, wenn `layer=comp`. Ignoriert durch Ebenen, die nicht mit einem Quellbild oder einer Maske verknüpft sind.

## Standard {#section-41f62d386c664f77952bc22e7286bb88}

Gesamtes Bild ( `cropN=0,0,1,1`).

## Beispiele {#section-2c99b481c0a04321979a3b522aa295d1}

**Beschneiden von 10 % links und 10 % rechts:**

`…&cropN=0.1,0,0.8,1&…`

**Beschneiden von 20 % am unteren Rand eines Bildes:**

`…&cropN=0,0,1,0.8&…`

## Verwandte Themen {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [expand=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
