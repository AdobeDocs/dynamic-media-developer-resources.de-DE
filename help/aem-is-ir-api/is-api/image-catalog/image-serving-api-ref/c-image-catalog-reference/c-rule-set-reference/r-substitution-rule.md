---
description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
seo-description: Ersetzungszeichenfolgen-Element. Optional in <rule>-Elementen.
seo-title: Ersatz
solution: Experience Manager
title: Ersatz
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Ersatz{#substitution}

Ersetzungszeichenfolgen-Element. Optional in `<rule>`-Elementen.

## Attribute {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Keine.

## Daten {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Ersatzzeichenfolge.

## Beschreibung {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definiert eine Ersatzzeichenfolge für die übereinstimmende Zeichenfolge oder Teilzeichenfolge im Pfad oder in der Abfrage.

Wenn der Ausdruck &quot;pattern&quot;Unter-Ausdruck enthält (mit Klammern getrennt), wird die erste übereinstimmende Unterzeichenfolge durch die Ersatzzeichenfolge ersetzt. Wenn der Ausdruck &quot;pattern&quot;keine Unter-Ausdruck enthält, wird die gesamte übereinstimmende Zeichenfolge ersetzt.

Ist `<expression>` leer oder fehlt, wird die Ersatzzeichenfolge an den Pfad oder die Abfrage angehängt.

Ist `<substitution>` leer, wird die übereinstimmende Zeichenfolge oder Unterzeichenfolge entfernt. Wenn `<substitution>` nicht angegeben ist, wird der Pfad oder die Abfrage-Zeichenfolge nicht geändert.

>[!NOTE]
>
>Alle Übereinstimmungen im Eingabestring werden ersetzt, wenn `replace="all"` im Element `<rule>` angegeben ist, zu dem dieses `<substitution>` gehört. Standardmäßig wird nur die erste Übereinstimmung durch die Ersatzzeichenfolge ersetzt.

## Hinweis {#section-cedf2adabaaf441c9f598fb0ea180246}

Die Ersatzzeichenfolge darf keine wörtlichen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` kodiert werden, oder die gesamte Zeichenfolge kann in einen XML-CDATA-Abschnitt eingeschlossen werden:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
