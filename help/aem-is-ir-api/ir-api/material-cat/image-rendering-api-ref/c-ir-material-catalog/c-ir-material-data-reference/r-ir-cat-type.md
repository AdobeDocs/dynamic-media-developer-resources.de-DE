---
description: Materialtyp. Oberflächenart des Materials. Wird zusammen mit Katalog-Gloss und Katalog-Roughness verwendet, um 3D Reflektion Rendereffekte zu steuern.
solution: Experience Manager
title: Typ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 912e2535-9980-4174-bca7-f44789eb39b4
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 18%

---

# Typ{#type}

Materialtyp. Oberflächenart des Materials. Wird zusammen mit catalog::Gloss und catalog::Roughness verwendet, um 3D-Reflektion Rendereffekte zu steuern.

## Eigenschaften {#section-86e8bc194f764c848e0ee55630a5ac1b}

Enum. Optional für alle Materialien. Wird ignoriert, wenn die Vignette keine 3D-Reflektion-Rendering-Funktion aufweist.

<table id="simpletable_85BF61871CAA420B92B855AAB8FACA2C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Unbekannt: Server verwendet den Standard. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Sonstige. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Naturholz. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Poliertes Metall. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Metall gebürstet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Antiquiertes Metall. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Farbe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Email/Lacquer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Hintergrund. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Plastik. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>Feste Oberfläche. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>Laminat. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>Vinyl. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>Keramik. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>Naturstein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>Glas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>Mirror. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>Stoff. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>Gewebe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Teppich. </p> </td> 
 </tr> 
</table>

## Standard {#section-247f73b22cb846b7b7d7cc6e8af949ca}

0; der Server bestimmt einen geeigneten Standard basierend auf anderen materiellen Attributen.

## Verwandte Themen {#section-a51850093b7140e683a0f8b07845843c}

[catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)
