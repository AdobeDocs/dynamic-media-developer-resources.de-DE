---
description: Decal size. Gibt die Größe eines Decalmaterials an.
solution: Experience Manager
title: Größe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# Größe{#size}

Decal size. Gibt die Größe eines Decalmaterials an.

` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Breite, Höhe  </span> </p> </td> 
  <td class="stentry"> <p>Größe des Decal-Objekts in Koordinateneinheiten der Szene (normalerweise Zoll) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness  </span> </p> </td> 
  <td class="stentry"> <p>Dicke des Decal-Objekts in Koordinateneinheiten der Szene (normalerweise Zoll) (real). </p> </td> 
 </tr> 
</table>

Wenn weder die Breite noch die Höhe 0 beträgt, wird das Bild auf die genauen angegebenen Abmessungen skaliert und das Seitenverhältnis des Bildes wird nicht beibehalten. Wenn einer der Werte auf 0 gesetzt wird, wird das Seitenverhältnis des Bildes beibehalten.

Wenn *`thickness`* angegeben ist, wird ein Schlagschatten gerendert, wenn das Vignettenobjekt einen entsprechenden Lichtvektor definiert. Setzen Sie *`thickness`* auf 0 , um das Rendering von Schlagschatten zu deaktivieren.

## Eigenschaften {#section-818e01e91fed4015951189c818ef28d8}

Materialattribut. Nur bei Dezimalstellen verwendet; von allen anderen Materialien ignoriert. `res=` wird ignoriert, wenn die Breite oder Höhe größer als 0 ist. Die Werte dürfen nicht negativ sein.

## Standard {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` wenn das Material auf einem Katalogeintrag basiert; andernfalls  `size=0,0,0`. Die Dekorgröße wird von `res=` berechnet, wenn *`wid`* und *`hei`* nicht angegeben sind oder auf 0 gesetzt sind. Wenn *`thickness`* nicht angegeben oder auf 0 gesetzt ist, wird kein Schlagschatten gerendert.

## Beispiel {#section-04fdc2b60b9e4071b672bf6a913738ad}

Ein MSS für einen Decal, der basierend auf der Auflösung skaliert, um 20° im Uhrzeigersinn gedreht und eine Dicke von 2,5 Zoll aufweist und für einen geeigneten Schlagschatteneffekt sorgt:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Verwandte Themen {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Scene Coordinates](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1),  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
