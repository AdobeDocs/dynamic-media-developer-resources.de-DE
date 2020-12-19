---
description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
seo-description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
seo-title: Allgemeine Datentypen
solution: Experience Manager
title: Allgemeine Datentypen
topic: Scene7 Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Allgemeine Datentypen{#common-data-types}

Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.

**Farbe**

Farbwert. Hexadezimaler, gepackter RGB-Wert, optional mit vorangestelltem Wert 0x. Der RGB-Wert `128,255,0` kann beispielsweise als `0x80ff00` oder `80ff00` angegeben werden.

**Markierung**

`0`=false,  `1`=true, bedeutet jeder andere Wert unbekannt oder nicht angegeben.

**Enum**

0 steht für einen unbekannten oder nicht angegebenen Wert, der mit einem leeren Feld identisch ist. Gültige Werte für `enum` sind fortlaufende Ganzzahlwerte, beginnend mit 1.

**Ganzzahl**

Signierter ganzzahliger Wert (z. B. 0, -12, 34). 0 oder negative Werte können eine besondere Bedeutung haben.

**Real number**

Unterschriebene Gleitkommawerte (z. B. `0, 12.5, 245 , -2.34e4`). 0 oder negative Werte können eine besondere Bedeutung haben.

**Textzeichenfolge**

Stringtrennzeichen sind optional, es sei denn, die Zeichenfolge enthält `<CR>`-, `<LF>`- oder `<TAB>`-Zeichen. Einfache und Dubletten-Anführungszeichen können als Trennzeichen verwendet werden. Wenn Anführungszeichen verwendet werden, muss jedes in die Zeichenfolge eingebettete Anführungszeichen mit zwei aufeinander folgenden Anführungszeichen (z. B. &#39; `This month''s Special`&#39;).
