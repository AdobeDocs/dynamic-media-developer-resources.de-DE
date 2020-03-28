---
description: Scharfzeichnen. Scharfzeichnen-Attribut bestimmt, wann das Material beim Rendern scharfgezeichnet wird.
seo-description: Scharfzeichnen. Scharfzeichnen-Attribut bestimmt, wann das Material beim Rendern scharfgezeichnet wird.
seo-title: Scharf
solution: Experience Manager
title: Scharf
topic: Scene7 Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Scharf{#sharp}

Scharfzeichnen. Scharfzeichnen-Attribut bestimmt, wann das Material beim Rendern scharfgezeichnet wird.

Art und Umfang des Scharfzeichnens werden durch die Vignette über eine Standard-Materialvorlage oder mit `catalog::RenderSettings`gesteuert.

## Eigenschaften {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Kein Scharfzeichnen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Normale Scharfzeichnung (nach der Transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alternative Scharfzeichnung (vor der Transformation). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Stärkere Scharfzeichnung (vor und nach der Transformation). </p></td> 
 </tr> 
</table>

Durch feste Farbstoffe ignoriert, optional für alle anderen Materialien.

## Standard {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` wird verwendet, wenn das Feld nicht vorhanden ist, leer ist oder wenn der Wert keine der unterstützten Optionen ist.

## Verwandte Themen {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[Attribut::Scharfzeichnen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [Katalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
