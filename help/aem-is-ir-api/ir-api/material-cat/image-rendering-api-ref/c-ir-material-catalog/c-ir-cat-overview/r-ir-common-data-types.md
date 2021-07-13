---
description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
solution: Experience Manager
title: Allgemeine Datentypen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Allgemeine Datentypen{#common-data-types}

Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.

**Farbe**

Farbwert. Hexadezimaler, gepackter RGB-Wert, optional mit vorangestelltem 0x. Beispielsweise kann der RGB-Wert `128,255,0` als `0x80ff00` oder `80ff00` angegeben werden.

**Markierung**

`0`=false,  `1`=true, bedeutet jeder andere Wert unbekannt oder nicht angegeben.

**Enum**

0 steht für einen unbekannten oder nicht angegebenen Wert, der mit einem leeren Feld übereinstimmt. Gültige `enum` -Werte sind aufeinander folgende Ganzzahlzahlen, beginnend bei 1.

**Ganzzahl**

Signierter ganzzahliger Wert (z. B. 0, -12, 34). 0 oder negative Werte können eine besondere Bedeutung haben.

**Real number**

Signierter Gleitkommawert (z. B. `0, 12.5, 245 , -2.34e4`). 0 oder negative Werte können eine besondere Bedeutung haben.

**Textzeichenfolge**

Zeichenfolgentrennzeichen sind optional, es sei denn, die Zeichenfolge enthält beliebige Zeichen `<CR>`, `<LF>` oder `<TAB>`. Einfache und doppelte Anführungszeichen können als Trennzeichen verwendet werden. Wenn Anführungszeichen verwendet werden, muss jedes in die Zeichenfolge eingebettete Anführungszeichen durch zwei aufeinander folgende Anführungszeichen (z. B. &#39; `This month''s Special`&#39;).
