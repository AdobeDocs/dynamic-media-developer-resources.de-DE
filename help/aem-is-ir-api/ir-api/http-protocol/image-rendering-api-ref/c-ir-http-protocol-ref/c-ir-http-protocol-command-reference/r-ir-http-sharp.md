---
title: scharf
description: Scharfzeichnen Sie die Textur. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 6%

---

# scharf{#sharp}

Scharfzeichnen Sie die Textur. Gibt die Scharfzeichnung an, die beim Rendern dieses Materials angewendet werden soll.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Keine Scharfzeichnung. </p> </td> 
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
  <td class="stentry"> <p>Mehr Scharfzeichnung (früh und spät). </p> </td> 
 </tr> 
</table>

`sharp=1` Wendet Scharfzeichnen an, nachdem das Material gerendert wurde; `sharp=2` wendet die Scharfzeichnung nach der anfänglichen Skalierung der Textur an, bevor sie in die Szene umgewandelt wird; `sharp=3` wendet die Scharfzeichnung sowohl vor als auch nach der Transformation an.

Der Scharfzeichnungsalgorithmus und die Menge der Scharfzeichnung und andere USM-Parameter (Unschärfemaske) werden durch die Standard-Materialvorlage gesteuert, die von der Vignette oder mit `rs=`.

## Eigenschaften {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Materialattribut. Ignoriert durch feste Farbstoffe.

## Standard {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, wenn das Material auf einem Katalogeintrag basiert, andernfalls `attribute::Sharp`.

## Verwandte Themen {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog: Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
