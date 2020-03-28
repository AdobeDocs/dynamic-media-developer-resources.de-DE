---
description: Bild beschneiden. Gibt einen rechteckigen Beschneidungsbereich an, der entweder in Pixel oder relativ zum Quellbild oder zum Maskenbild mit voller Auflösung normalisiert wird.
seo-description: Bild beschneiden. Gibt einen rechteckigen Beschneidungsbereich an, der entweder in Pixel oder relativ zum Quellbild oder zum Maskenbild mit voller Auflösung normalisiert wird.
seo-title: Zuschneiden
solution: Experience Manager
title: Zuschneiden
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Zuschneiden{#crop}

Bild beschneiden. Gibt einen rechteckigen Beschneidungsbereich an, der entweder in Pixel oder relativ zum Quellbild oder zum Maskenbild mit voller Auflösung normalisiert wird.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`coordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Koffer</span></span> </p> </td> 
  <td class="stentry"> <p>Pixel-Offset von der oberen linken Ecke des Quellbilds nach links oben des Beschneidungsrects (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Normalisierter Offset von oben links im Quellbild nach oben links im Beschneidungsrect (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Größe</span></span> </p></td> 
  <td class="stentry"> <p>Größe des Beschneidungsrechtecks in Pixel (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Die normalisierte Größe des Beschneidungsprotokolls im Verhältnis zur Größe des Quellbilds (real, real). </p></td> 
 </tr> 
</table>

Kann auch verwendet werden, um das Bild über seine Grenzen hinaus durch Angabe negativer x-, y- und/oder width-, height-Werte größer als die Bildbreite und -höhe. In diesem Fall ist der erweiterte Bereich vollständig transparent (sofern nicht `bgColor=` angegeben).

## Eigenschaften {#section-632e0405bb9940679b5f8b1c10e0902e}

Quellenbild/Maskenattribut. Gilt für das Quellbild der Ebene 0, wenn `layer=comp`dies der Fall ist. Ignoriert von Ebenen, die nicht mit einem Quellbild oder einer Quellmaske verknüpft sind.

## Standard {#section-41f62d386c664f77952bc22e7286bb88}

Gesamtes Bild ( `cropN=0,0,1,1`).

## Beispiele {#section-2c99b481c0a04321979a3b522aa295d1}

**Beschneiden Sie 10 % links und 10 % rechts:**

`…&cropN=0.1,0,0.8,1&…`

**Beschneiden Sie 20 % vom unteren Rand eines Bilds:**

`…&cropN=0,0,1,0.8&…`

## Verwandte Themen {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cutPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
