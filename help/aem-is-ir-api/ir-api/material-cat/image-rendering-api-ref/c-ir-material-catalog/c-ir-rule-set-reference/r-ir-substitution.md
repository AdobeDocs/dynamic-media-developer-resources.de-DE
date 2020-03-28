---
description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
seo-description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
seo-title: Ersatz
solution: Experience Manager
title: Ersatz
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Ersatz{#substitution}

Ersetzungszeichenfolgen-Element. Optional in `<rule>` Elementen.

## Attribute {#section-d955eefc53eb4274861270669c01f9ca}

Keine.

## Daten {#section-a2688866ed6d41279a8478886e511ae3}

Ersatzzeichenfolge.

## Beschreibung {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definiert eine Ersatzzeichenfolge für die übereinstimmende Zeichenfolge oder Unterzeichenfolge im Pfad oder in der Abfrage.

Wenn der Ausdruck &quot;pattern&quot;Unterabschnitte (mit Klammern getrennt) enthält, wird die erste übereinstimmende Unterzeichenfolge durch die Ersatzzeichenfolge ersetzt. Wenn der Ausdruck &quot;pattern&quot;keine Unter-Ausdruck enthält, wird die gesamte übereinstimmende Zeichenfolge ersetzt.

Ist `<expression>` der Wert leer oder fehlt er, wird die Ersatzzeichenfolge an den Pfad oder die Abfrage angehängt.

Wenn `<substitution>` der Wert leer ist, wird die übereinstimmende Zeichenfolge oder Unterzeichenfolge entfernt. Wenn `<substitution>` keine Angabe gemacht wird, wird der Pfad oder die Zeichenfolge der Abfrage nicht geändert.

## Hinweis {#section-90fe89bb17a04804b7ff3c93df082892}

Die Ersatzzeichenfolge darf keine wörtlichen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<`kodiert werden, oder die gesamte Zeichenfolge kann in einen XML- `CDATA` Abschnitt eingeschlossen werden:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
