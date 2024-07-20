---
title: Allgemeine Datentypen
description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Allgemeine Datentypen{#common-data-types}

Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.

**Farbe**

Farbwert. Hexadezimaler, gepackter RGB-Wert, optional mit 0x vorangestellt. Beispielsweise kann der RGB-Wert `128,255,0` als `0x80ff00` oder `80ff00` angegeben werden.

**Flag**

`0`=false, `1`=true, jeder andere Wert bedeutet unbekannt oder nicht angegeben.

**Enum**

`0` gibt einen unbekannten oder unspezifizierten Wert an, der mit einem leeren Feld übereinstimmt. Gültige Werte vom Typ `enum` sind aufeinander folgende Ganzzahlen, beginnend bei 1.

**Ganzzahl**

Signierter Ganzzahlwert (z. B. `0, -12, 34`). `0` oder negative Werte können eine besondere Bedeutung haben.

**Real number**

Signierter Gleitkommawert (z. B. `0, 12.5, 245 , -2.34e4`). 0 oder negative Werte können eine besondere Bedeutung haben.

**Textzeichenfolge**

Zeichenfolgentrennzeichen sind optional, es sei denn, die Zeichenfolge enthält beliebige `<CR>`-, `<LF>`- oder `<TAB>`-Zeichen. Einfache und doppelte Anführungszeichen können als Trennzeichen verwendet werden. Wenn Anführungszeichen verwendet werden, muss jedes in die Zeichenfolge eingebettete Anführungszeichen durch zwei aufeinander folgende Anführungszeichen (z. B. &quot;`This month''s Special`&quot;) maskiert werden.
