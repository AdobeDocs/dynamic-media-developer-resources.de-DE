---
description: Alle Schriftarten, auf die in der RTF-Zeichenfolge verwiesen wird, müssen in der Schriftartzuordnungsdatei des Standardkatalogs oder des aktuellen Bildkatalogs verfügbar sein. Andernfalls wird ein Fehler zurückgegeben.
solution: Experience Manager
title: Schriftverarbeitung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# Schriftverarbeitung{#font-handling}

Alle Schriftarten, auf die in der RTF-Zeichenfolge verwiesen wird, müssen in der Schriftartzuordnungsdatei des Standardkatalogs oder des aktuellen Bildkatalogs verfügbar sein. Andernfalls wird ein Fehler zurückgegeben.

Die beste Qualität für kursiv und fett gedruckten Text wird durch die Registrierung der entsprechenden Schriftartendateien erreicht. Falls nicht verfügbar, kann der Server fett und/oder kursiv gedruckte Schriftarten von der Standardseite aus synthetisieren. (Siehe ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

Die mit `attribute::DefaultFont` angegebene Schriftart wird verwendet, wenn keine explizit in der RTF-Zeichenfolge angegeben ist.

Image Serving unterstützt TrueType-, OpenType- und Adobe Type 1-Schriftarten (nur Windows).

## Unterstützung von Fotofont®-Schriftarten {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` unterstützt Fotofont®-Schriftarten mit den folgenden Einschränkungen:

* `\cf` wird in Textbereichen ignoriert, die eine Fotoschriftart angeben; Schriftarten mit vordefinierten Farben
* Synthesierte Schriftstile werden nicht unterstützt. Verwendung von `\b` und `\i`erfordert entsprechende Schriftzuordnungseinträge, andernfalls wird ein Fehler zurückgegeben

* Vertikaler Textfluss wird nicht unterstützt
* Fotoschriftarten mit 16-Bit-Bildern werden nicht unterstützt
* Schriftarten mit mehreren Symbolen pro Bild werden nicht unterstützt
* Es wird eine naïve Farbkonvertierung angewendet, es sei denn, die Farbprofile für die Fotoschrift-Glyphbilder werden eingebettet. in diesem Fall werden immer die relative farbmetrische Renderpriorität und die Blackpoint-Kompensation angewendet.

Weitere Informationen finden Sie unter [www.photofont.com](https://www.photofont.com).

## Verwandte Themen {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d),  [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](https://www.photofont.com)
