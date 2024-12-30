---
title: überziehen
description: Farbe und Stärke des Fliesenmörtels. Simuliert Fugenmörtel für Keramik- und Natursteinfliesen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# überziehen {#grout}

Farbe und Stärke des Fliesenmörtels. Simuliert Fugenmörtel für Keramik- und Natursteinfliesen.

Mörtel= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Farbe </span> </span> </p> </td>
  <td class="stentry"> <p>Fugenfarbe (grau oder RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Breite </span> </span> </p> </td>
  <td class="stentry"> <p>Fugendicke; Szenen-Koordinateneinheiten (normalerweise Zoll) (real). </p> </td>
 </tr> 
</table>

Für eine möglichst gute Kontrolle des Aussehens der Mörtel gelten folgende Anforderungen:

* Die Kachel muss quadratisch oder rechteckig sein; derzeit werden keine anderen Formen unterstützt.
* Das Bild darf nur eine einzige Kachel enthalten.
* Die Standardfuge im Bild (falls vorhanden) muss an allen vier Kanten gleich dick sein.
* Die Stärke des Mörtels muss im Materialkatalog (`catalog::GroutWidth`) angegeben werden.

## Eigenschaften {#section-de78b678245b4ffda48097c345949e77}

Materialattribut. `*`color`*` Muss ein RGB-Farbwert sein. `*`Breite`*` muss ein reeller Wert von 0 oder höher sein.

Ignoriert, wenn Wiederholung = 4, 5, 7, 8, 9, 14 oder höher ist oder wenn für andere Materialien als wiederholbare Texturen angegeben.

## Standard {#section-bfab3621f70b4489a21994ab11b20cc6}

Wenn `grout=` nicht angegeben ist, wird der Mörtel im Bild nicht geändert. Wenn `grout= *`color`*` angegeben ist, wird `*`width`*` standardmäßig auf `catalog::GroutWidth` gesetzt.

## Verwandte Themen {#section-8d472906a44943f5a8557e98f2fbc71f}

[Farbwerte](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
