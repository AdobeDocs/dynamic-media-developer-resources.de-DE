---
description: Materielle Oberflächenrauigkeit. Gibt die relative Rauigkeit der Materialoberfläche an.
seo-description: Materielle Oberflächenrauigkeit. Gibt die relative Rauigkeit der Materialoberfläche an.
seo-title: rau
solution: Experience Manager
title: rau
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rau{#rough}

Materielle Oberflächenrauigkeit. Gibt die relative Rauigkeit der Materialoberfläche an.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Oberflächenrauigkeit (0...100 Prozent) oder -1 zur Auswahl der Standardrauigkeit. </p> </td> 
 </tr> 
</table>

Dient zum Steuern des Rendereffekts der 3D-Reflektion. Niedrigere Rauschwerte führen in der Regel zu glatteren Reflexionseffekten. höhere Werte führen zu Randomisierung und Streuung des reflektierten Bildes.

Jeder Werkstofftyp ( `type=`) definiert einen minimalen und einen maximalen Reflektionseffekt basierend auf Rauigkeit. Bei einigen Materialarten (z.B. Wandpapier) hat `rough=` es kaum Auswirkungen auf das Erscheinungsbild der Reflektion, während bei anderen Materialtypen (z.B. Stein oder Keramik) der Effekt wesentlich ausgeprägter ist.

`rough=-1` setzt die Rauigkeit auf einen serverinternen Standardwert (40 % bei typischen Materialtypen).

## Eigenschaften {#section-515375758b254c80af576271bdb61bb8}

Materialattribut. Wird ignoriert, wenn die Vignette keine 3D-Reflektionsfähigkeit besitzt, wenn dem Objekt &quot;Zielgruppe&quot;keine 3D-Geometrie zugeordnet ist oder wenn das Objekt &quot;Zielgruppe&quot;keine anderen Objekte in der Szene widerspiegelt.

## Standard {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` wenn das Material auf einem Katalogeintrag basiert, andernfalls ca. 40 %.

## Verwandte Themen {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
