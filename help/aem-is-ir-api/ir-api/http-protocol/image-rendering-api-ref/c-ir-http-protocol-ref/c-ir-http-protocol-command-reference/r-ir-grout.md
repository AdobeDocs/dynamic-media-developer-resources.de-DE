---
description: Farbe und Dicke der Kachelgrotte. Simuliert Grout für Keramik und Naturstein Fliesen.
solution: Experience Manager
title: grout
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# grout{#grout}

Farbe und Dicke der Kachelgrotte. Simuliert Grout für Keramik und Naturstein Fliesen.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Grout-Farbe (grau oder RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Bodendicke; Koordinateneinheiten der Szene (normalerweise Zoll) (real). </p> </td> 
 </tr> 
</table>

Für eine maximale Kontrolle des Aussehens der Grout gelten folgende Anforderungen:

* Die Kachel muss quadratisch oder rechteckig sein; Derzeit werden keine anderen Formen unterstützt.
* Das Bild darf nur eine Kachel enthalten.
* Die Standardbreite im Bild (falls vorhanden) muss an allen vier Kanten genau dieselbe Dicke aufweisen.
* Die Dicke der Standardgruppe muss im Materialkatalog ( `catalog::GroutWidth`) angegeben werden.

## Eigenschaften {#section-de78b678245b4ffda48097c345949e77}

Materialattribut. `*``*` color muss ein RGB-Farbwert sein. `*``*` muss einen realen Wert von 0 oder größer sein.

Ignoriert bei Wiederholung = 4, 5, 7, 8, 9, 14 oder höher oder bei Materialien, die keine wiederholbaren Texturen sind.

## Standard {#section-bfab3621f70b4489a21994ab11b20cc6}

Wenn `grout=` nicht angegeben ist, wird die Grout im Bild nicht geändert. Wenn ` grout= *`color`*` angegeben ist, wird `*`width`*` standardmäßig auf `catalog::GroutWidth` gesetzt.

## Verwandte Themen {#section-8d472906a44943f5a8557e98f2fbc71f}

[Farbwerte](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
