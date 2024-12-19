---
title: Größe
description: Abziehbildgröße. Gibt die Größe eines Abziehbilds an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 2%

---

# Größe{#size}

Abziehbildgröße. Gibt die Größe eines Abziehbilds an.

` size= *`Breite,Höhe`*[ *`,Stärke`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Breite, Höhe </span> </p> </td> 
  <td class="stentry"> <p>Größe des Abziehbildobjekts in Szenenkoordinateneinheiten (normalerweise Zoll) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Die Dicke des Abziehbilds in Szenenkoordinateneinheiten (normalerweise in Zoll) (real). </p> </td> 
 </tr> 
</table>

Wenn weder Breite noch Höhe 0 beträgt, wird das Bild auf die exakt angegebenen Abmessungen skaliert und das Seitenverhältnis des Bildes wird nicht beibehalten. Wenn Sie einen der Werte auf 0 setzen, bleibt das Seitenverhältnis des Bildes erhalten.

Wenn *`thickness`* angegeben ist, wird ein Schlagschatten gerendert, wenn das Vignettenobjekt einen geeigneten Lichtvektor definiert. Legen Sie *`thickness`* auf 0 fest, um das Drop-Shadow-Rendering zu deaktivieren.

## Eigenschaften {#section-818e01e91fed4015951189c818ef28d8}

Materialattribut. Wird nur von Abziehbildern verwendet; wird von allen anderen Materialien ignoriert. `res=` wird ignoriert, wenn entweder Breite oder Höhe größer als 0 ist. Werte dürfen nicht negativ sein.

## Standard {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size`, ob das Abziehmaterial auf einem Katalogeintrag basiert; andernfalls `size=0,0,0`. Die Abziehbildgröße wird aus `res=` berechnet, wenn *`wid`* und *`hei`* nicht angegeben oder auf 0 gesetzt sind. Es wird kein Schlagschatten gerendert, wenn *`thickness`* nicht angegeben oder auf 0 gesetzt ist.

## Beispiel {#section-04fdc2b60b9e4071b672bf6a913738ad}

Ein MSS für ein Abziehbild, dessen Größe auf der Auflösung basiert, um 20 Grad im Uhrzeigersinn gedreht wird und eine Dicke von 2,5 Zoll hat, für einen geeigneten Tropfenschatteneffekt:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Verwandte Themen {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Szenenkoordinaten](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
