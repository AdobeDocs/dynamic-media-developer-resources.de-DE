---
description: Kachelgrottenfarbe und -dicke. Simuliert die Leiste für keramische und natürliche Steinplatten.
seo-description: Kachelgrottenfarbe und -dicke. Simuliert die Leiste für keramische und natürliche Steinplatten.
seo-title: Ground
solution: Experience Manager
title: Ground
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ground{#grout}

Kachelgrottenfarbe und -dicke. Simuliert die Leiste für keramische und natürliche Steinplatten.

Grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Farbe </span></span> </p> </td> 
  <td class="stentry"> <p>Grundfarbe (grau oder RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Bodendicke; Koordinateneinheiten der Szene (normalerweise Zoll) (real). </p> </td> 
 </tr> 
</table>

Für eine maximale Kontrolle des Aussehens des Bodens gelten folgende Anforderungen:

* Die Kachel muss quadratisch oder rechteckig sein. Derzeit werden keine anderen Formen unterstützt.
* Das Bild darf nur eine Kachel enthalten.
* Die Standarddicke im Bild (sofern vorhanden) muss an allen vier Kanten exakt dieselbe Stärke aufweisen.
* Die Stärke des Standardteils muss im Materialkatalog ( `catalog::GroutWidth`) angegeben werden.

## Eigenschaften {#section-de78b678245b4ffda48097c345949e77}

Materialattribut. ` *`color`*` muss ein RGB-Farbwert sein. ` *`width`*` muss ein echter Wert 0 oder größer sein.

Wird ignoriert, wenn &quot;Repeat = 4, 5, 7, 8, 9, 14 oder höher&quot;oder bei anderen Materialien als wiederholbaren Texturen angegeben.

## Standard {#section-bfab3621f70b4489a21994ab11b20cc6}

Wenn `grout=` keine Angabe gemacht wird, wird der Grund im Bild nicht geändert. Wenn ` grout= *`Farbe`*` angegeben ist, wird ` *`Breite`*` standardmäßig `catalog::GroutWidth`.

## Verwandte Themen {#section-8d472906a44943f5a8557e98f2fbc71f}

[Farbwerte](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
