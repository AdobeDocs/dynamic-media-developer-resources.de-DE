---
title: Allgemeine Datentypen
description: Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# Allgemeine Datentypen{#common-data-types}

Katalogattribute und -felder können Daten eines der folgenden Typen enthalten.

**color**

Farbwert. Hexadezimaler, gepackter RGB-Wert, optional mit vorangestelltem 0x. Beispielsweise kann der RGB-`128,255,0` als `0x80ff00` oder `80ff00` angegeben werden.

**Flag**

`0`=false, `1`=true, jeder andere Wert bedeutet unbekannt oder nicht angegeben.

**enum**

`0` gibt einen unbekannten oder nicht angegebenen Wert an, genauso wie ein leeres Feld. Gültige `enum` sind aufeinander folgende Ganzzahlen, beginnend mit 1.

**Ganzzahl**

Ganzzahliger Wert mit Vorzeichen (z. B. `0, -12, 34`). `0` oder negative Werte können eine besondere Bedeutung haben.

**Reelle Zahl**

Vorzeichenmäßiger Gleitkommawert (z. B. `0, 12.5, 245 , -2.34e4`). 0 oder negative Werte können eine besondere Bedeutung haben.

**Textzeichenfolge**

Zeichenfolgen-Trennzeichen sind optional, es sei denn, die Zeichenfolge enthält `<CR>`, `<LF>` oder `<TAB>` Zeichen. Als Trennzeichen können einfache und doppelte Anführungszeichen verwendet werden. Wenn Anführungszeichen verwendet werden, müssen alle solchen in die Zeichenfolge eingebetteten Anführungszeichen mithilfe von zwei aufeinander folgenden Anführungszeichen maskiert werden (z. B. &quot;`This month''s Special`„).
