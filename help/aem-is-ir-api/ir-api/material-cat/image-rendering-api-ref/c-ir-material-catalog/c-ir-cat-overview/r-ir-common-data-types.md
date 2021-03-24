---
description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
solution: Experience Manager
title: Allgemeine Datentypen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
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
