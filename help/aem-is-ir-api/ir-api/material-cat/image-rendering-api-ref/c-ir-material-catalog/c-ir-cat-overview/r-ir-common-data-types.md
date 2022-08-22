---
title: Allgemeine Datentypen
description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Allgemeine Datentypen{#common-data-types}

Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.

**Farbe**

Farbwert. Hexadezimaler, gepackter RGB-Wert, optional mit 0x vorangestellt. Beispielsweise der RGB-Wert `128,255,0` kann als `0x80ff00` oder `80ff00`.

**Markierung**

`0`=false, `1`den Wert &quot;true&quot;hat, bedeutet jeder andere Wert &quot;unbekannt&quot;oder &quot;unspezifisch&quot;.

**Enum**

`0` bezeichnet einen unbekannten oder unspezifizierten Wert, der mit einem leeren Feld übereinstimmt. Gültig `enum` -Werte sind aufeinander folgende ganzzahlige Zahlen, beginnend bei 1.

**Ganzzahl**

Signierter ganzzahliger Wert (z. B. `0, -12, 34`). `0` oder negative Werte können eine besondere Bedeutung haben.

**Real number**

Signierter Gleitkommawert (z. B. `0, 12.5, 245 , -2.34e4`). 0 oder negative Werte können eine besondere Bedeutung haben.

**Textzeichenfolge**

Zeichenfolgentrennzeichen sind optional, es sei denn, die Zeichenfolge enthält eine `<CR>`, `<LF>`oder `<TAB>` Zeichen. Einfache und doppelte Anführungszeichen können als Trennzeichen verwendet werden. Wenn Anführungszeichen verwendet werden, muss jedes in die Zeichenfolge eingebettete Anführungszeichen durch zwei aufeinander folgende Anführungszeichen maskiert werden (z. B. &quot; `This month''s Special`&quot;).
