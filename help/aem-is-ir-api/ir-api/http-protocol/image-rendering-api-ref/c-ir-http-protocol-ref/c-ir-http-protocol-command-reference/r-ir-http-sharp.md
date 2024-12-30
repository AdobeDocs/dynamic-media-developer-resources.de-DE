---
title: stechend
description: Textur schärfen. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# stechend{#sharp}

Textur schärfen. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.

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
  <td class="stentry"> <p>0 alternative Scharfzeichnung (früh). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Weitere Scharfzeichnung (früh und spät). </p> </td> 
 </tr> 
</table>

`sharp=1` Wendet die Scharfzeichnung nach dem Rendern des Materials an; `sharp=2` wendet die Scharfzeichnung nach der ersten Skalierung der Textur an, aber bevor sie in die Szene umgewandelt wird; `sharp=3` wendet die Scharfzeichnung sowohl vor als auch nach der Transformation an.

Der Scharfzeichnungsalgorithmus und die Menge der Scharfzeichnungsund anderen USM-Parameter (Unschärfemasken) werden von der standardmäßigen Materialvorlage gesteuert, die von der Vignette oder mit `rs=` bereitgestellt wird.

## Eigenschaften {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Materialattribut. Von einfarbigen Materialien ignoriert.

## Standard {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, wenn das Material auf einem Katalogeintrag basiert, andernfalls `attribute::Sharp`.

## Verwandte Themen {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
