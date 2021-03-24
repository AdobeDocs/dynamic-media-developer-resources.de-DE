---
description: Kachelgrottenfarbe und -dicke. Simuliert die Leiste für keramische und natürliche Steinplatten.
solution: Experience Manager
title: Ground
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---


# grout{#grout}

Kachelgrottenfarbe und -dicke. Simuliert die Leiste für keramische und natürliche Steinplatten.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
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

Materialattribut. `*`Die `*` Farbe muss ein RGB-Farbwert sein. `*`Die `*` Breite muss einen realen Wert 0 oder größer sein.

Wird ignoriert, wenn &quot;Repeat = 4, 5, 7, 8, 9, 14 oder höher&quot;oder bei anderen Materialien als wiederholbaren Texturen angegeben.

## Standard {#section-bfab3621f70b4489a21994ab11b20cc6}

Wenn `grout=` nicht angegeben ist, wird der Grund im Bild nicht geändert. Wenn ` grout= *`color`*` angegeben ist, wird `*`width`*` standardmäßig auf `catalog::GroutWidth` gesetzt.

## Verwandte Themen {#section-8d472906a44943f5a8557e98f2fbc71f}

[Farbwerte](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
