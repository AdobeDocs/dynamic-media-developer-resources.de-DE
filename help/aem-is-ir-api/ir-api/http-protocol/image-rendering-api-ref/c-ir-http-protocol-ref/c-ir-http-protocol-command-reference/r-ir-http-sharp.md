---
description: Scharfzeichnen der Textur. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.
seo-description: Scharfzeichnen der Textur. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.
seo-title: spitze
solution: Experience Manager
title: spitze
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 5%

---


# sharp{#sharp}

Scharfzeichnen der Textur. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Kein Scharfzeichnen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Normale Scharfzeichnung (spät). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 alternatives Scharfzeichnen (früh). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Mehr Scharfzeichnen (früh und spät). </p> </td> 
 </tr> 
</table>

`sharp=1` das Scharfzeichnen nach der Wiedergabe des Materials vornimmt;  `sharp=2` wendet das Scharfzeichnen nach der anfänglichen Skalierung der Textur an, bevor sie jedoch in die Szene umgewandelt wird;  `sharp=3` Wendet Scharfzeichnen vor und nach der Transformation an.

Der Scharfzeichnungsalgorithmus und die Schärfungsmenge sowie andere USM-Parameter (Unschärfemaske) werden durch die Standardmateriellvorlage gesteuert, die von der Vignette oder mit `rs=` bereitgestellt wird.

## Eigenschaften {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Materialattribut. Wird von festen Farbstoffen ignoriert.

## Standard {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, wenn das Material auf einem Katalogeintrag basiert, andernfalls  `attribute::Sharp`.

## Verwandte Themen {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[Katalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
