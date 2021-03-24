---
description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
solution: Experience Manager
title: Ersatz
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# Ersatz{#substitution}

Ersetzungszeichenfolgen-Element. Optional in `<rule>`-Elementen.

## Attribute {#section-d955eefc53eb4274861270669c01f9ca}

Keine.

## Daten {#section-a2688866ed6d41279a8478886e511ae3}

Ersatzzeichenfolge.

## Beschreibung {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definiert eine Ersatzzeichenfolge für die übereinstimmende Zeichenfolge oder Unterzeichenfolge im Pfad oder in der Abfrage.

Wenn der Ausdruck &quot;pattern&quot;Unterabschnitte (mit Klammern getrennt) enthält, wird die erste übereinstimmende Unterzeichenfolge durch die Ersatzzeichenfolge ersetzt. Wenn der Ausdruck &quot;pattern&quot;keine Unter-Ausdruck enthält, wird die gesamte übereinstimmende Zeichenfolge ersetzt.

Ist `<expression>` leer oder fehlt, wird die Ersatzzeichenfolge an den Pfad oder die Abfrage angehängt.

Ist `<substitution>` leer, wird die übereinstimmende Zeichenfolge oder Unterzeichenfolge entfernt. Wenn `<substitution>` nicht angegeben ist, wird der Pfad oder die Abfrage-Zeichenfolge nicht geändert.

## Hinweis {#section-90fe89bb17a04804b7ff3c93df082892}

Die Ersatzzeichenfolge darf keine wörtlichen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` kodiert werden, oder die gesamte Zeichenfolge kann in einen XML `CDATA`-Abschnitt eingeschlossen werden:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
