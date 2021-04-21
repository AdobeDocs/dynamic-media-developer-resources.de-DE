---
description: Alle Schriftarten, auf die in der RTF-Zeichenfolge verwiesen wird, müssen in der Schriftartzuordnungsdatei des Standardkatalogs oder des aktuellen Bildkatalogs verfügbar sein. Andernfalls wird ein Fehler zurückgegeben.
solution: Experience Manager
title: Schriftverarbeitung
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---


# Schriftverarbeitung{#font-handling}

Alle Schriftarten, auf die in der RTF-Zeichenfolge verwiesen wird, müssen in der Schriftartzuordnungsdatei des Standardkatalogs oder des aktuellen Bildkatalogs verfügbar sein. Andernfalls wird ein Fehler zurückgegeben.

Die beste Qualität für kursiven und fett gedruckten Text wird durch die Registrierung der entsprechenden Schriftartdateien erreicht. Ist dies nicht möglich, kann der Server fett und/oder kursiv gedruckte Schriftarten aus der Standardfläche synthetisieren. (Siehe ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

Die mit `attribute::DefaultFont` angegebene Schriftart wird verwendet, wenn keine explizit in der RTF-Zeichenfolge angegeben ist.

Image Serving unterstützt TrueType-, OpenType-, Adobe Type 1- (nur Windows) Schriftarten.

## Fotofont® font support {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` unterstützt Fotofont®-Schriftarten mit folgenden Einschränkungen:

* `\cf` wird in Textbereichen, die eine Fotoschriftart angeben, ignoriert; Schriftarten mit Fotoschrift haben vordefinierte Farben
* Synthetisierte Schriftschnitte werden nicht unterstützt. Verwendung von `\b` und `\i`erfordert entsprechende Schriftzuordnungseinträge, andernfalls wird ein Fehler zurückgegeben

* Vertikaler Textfluss wird nicht unterstützt
* Fotoschriftarten mit 16-Bit-Bildern werden nicht unterstützt
* Schriftarten mit mehreren Glyphen pro Bild werden nicht unterstützt
* Die Konvertierung naiver Farben wird angewendet, es sei denn, die Profile der Fotoschriftart-Glyphe betten Farbbilder ein. in diesem Fall werden die relative farbmetrische Renderpriorität und die Blackpoint-Kompensation immer angewendet

Weitere Informationen finden Sie unter ` [www.photofont.com](http://www.photofont.com)`.

## Verwandte Themen {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d),  [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
