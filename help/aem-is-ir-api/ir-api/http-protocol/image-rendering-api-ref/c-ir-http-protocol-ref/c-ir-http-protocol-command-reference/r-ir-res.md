---
title: res
description: Materialauflösung. Gibt die Auflösung der wiederholbaren Textur oder Abziehbild an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# res{#res}

Materialauflösung. Gibt die Auflösung der wiederholbaren Textur oder Abziehbild an.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Val </span> </p> </td> 
  <td class="stentry"> <p>Auflösung; Einheiten für die Materialauflösung (normalerweise Pixel pro Zoll) (real). </p> </td> 
 </tr> 
</table>

Wenn ein Abziehmaterial vorhanden ist, hat `size=` Vorrang, wenn sowohl `size=` als auch `res=` angegeben sind.

## Eigenschaften {#section-6a458ddc202f46e0b668c9f040a65cef}

Materialattribut. Von einfarbigen Materialien ignoriert. Nur durch Schrank- und Fensterbeläge Materialien nur, wenn auch eine Textur verwendet wird.

## Standard {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, wenn das Material auf einem Katalogeintrag basiert, andernfalls `attribute::Resolution`, wenn nicht angegeben oder auf einen Wert kleiner oder gleich 0 festgelegt `res= is`.

## Verwandte Themen {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Materialauflösung](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
