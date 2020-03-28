---
description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
seo-description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
seo-title: Ersatz
solution: Experience Manager
title: Ersatz
topic: Scene7 Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Ersatz{#substitution}

Ersetzungszeichenfolgen-Element. Optional in `<rule>` Elementen.

## Attribute {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Keine.

## Daten {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Ersatzzeichenfolge.

## Beschreibung {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definiert eine Ersatzzeichenfolge für die übereinstimmende Zeichenfolge oder Teilzeichenfolge im Pfad oder in der Abfrage.

Wenn der Ausdruck &quot;pattern&quot;Unter-Ausdruck enthält (mit Klammern getrennt), wird die erste übereinstimmende Unterzeichenfolge durch die Ersatzzeichenfolge ersetzt. Wenn der Ausdruck &quot;pattern&quot;keine Unter-Ausdruck enthält, wird die gesamte übereinstimmende Zeichenfolge ersetzt.

Ist `<expression>` der Wert leer oder fehlt er, wird die Ersatzzeichenfolge an den Pfad oder die Abfrage angehängt.

Wenn `<substitution>` der Wert leer ist, wird die übereinstimmende Zeichenfolge oder Unterzeichenfolge entfernt. Wenn `<substitution>` keine Angabe gemacht wird, wird der Pfad oder die Zeichenfolge der Abfrage nicht geändert.

>[!NOTE]
>
>Alle Übereinstimmungen im Eingabestring werden ersetzt, wenn sie im Element `replace="all"` , `<rule>`zu dem dieses `<substitution>` Element gehört, angegeben werden. Standardmäßig wird nur die erste Übereinstimmung durch die Ersatzzeichenfolge ersetzt.

## Hinweis {#section-cedf2adabaaf441c9f598fb0ea180246}

Die Ersatzzeichenfolge darf keine wörtlichen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<`kodiert werden, oder die gesamte Zeichenfolge kann in einen XML-CDATA-Abschnitt eingeschlossen werden:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
