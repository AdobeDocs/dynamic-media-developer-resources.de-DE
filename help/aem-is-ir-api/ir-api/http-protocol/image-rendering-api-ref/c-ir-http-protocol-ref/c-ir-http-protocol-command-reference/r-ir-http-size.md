---
description: Dezimalgröße. Gibt die Größe eines dekalen Materials an.
seo-description: Dezimalgröße. Gibt die Größe eines dekalen Materials an.
seo-title: Größe
solution: Experience Manager
title: Größe
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 3%

---


# Größe{#size}

Dezimalgröße. Gibt die Größe eines dekalen Materials an.

` size= *`Breite,Höhe`*[ *`,Stärke`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> width, height  </span> </p> </td> 
  <td class="stentry"> <p>Größe des dekalen Objekts in Koordinateneinheiten der Szene (normalerweise Zoll) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness  </span> </p> </td> 
  <td class="stentry"> <p>Stärke des dekalen Objekts in Koordinateneinheiten der Szene (typischerweise Zoll) (real). </p> </td> 
 </tr> 
</table>

Wenn weder die Breite noch die Höhe 0 beträgt, wird das Bild auf die exakt festgelegten Abmessungen skaliert und das Seitenverhältnis des Bilds wird nicht beibehalten. Wenn Sie einen der Werte auf 0 setzen, wird das Seitenverhältnis des Bilds beibehalten.

Wenn *`thickness`* angegeben ist, wird ein Schlagschatten gerendert, wenn das Vignettenobjekt einen entsprechenden Lichtvektor definiert. Setzen Sie *`thickness`* auf 0, um das Rendering von Schlagschatten zu deaktivieren.

## Eigenschaften {#section-818e01e91fed4015951189c818ef28d8}

Materialattribut. Nur von Aufklebern verwendet; von allen anderen Materialien ignoriert. `res=` wird ignoriert, wenn Breite oder Höhe größer als 0 ist. Die Werte dürfen nicht negativ sein.

## Standard {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` wenn das materielle Material auf einem Katalogeintrag basiert; andernfalls  `size=0,0,0`. Die Größe des Dezimalbereichs wird von `res=` berechnet, wenn *`wid`* und *`hei`* nicht angegeben sind oder auf 0 eingestellt sind. Es wird kein Schlagschatten gerendert, wenn *`thickness`* nicht angegeben oder auf 0 eingestellt ist.

## Beispiel {#section-04fdc2b60b9e4071b672bf6a913738ad}

Ein MSS für einen Abfall, der basierend auf der Auflösung skaliert, um 20° im Uhrzeigersinn gedreht und mit einer Stärke von 2,5 Zoll für einen geeigneten Schlagschatteneffekt gedreht wird:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Verwandte Themen {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Scene-Koordinaten](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1),  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [Attribut::Auflösung](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
