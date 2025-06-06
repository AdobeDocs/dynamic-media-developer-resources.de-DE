---
description: Ersatz-Zeichenfolgenelement. Optional in <rule>-Elementen.
solution: Experience Manager
title: Substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Substitution{#substitution}

Ersatz-Zeichenfolgenelement. Optional in `<rule>`.

## Attribute {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Keine.

## Daten {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Ersatzzeichenfolge.

## Beschreibung {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definiert eine Ersatzzeichenfolge für die übereinstimmende Zeichenfolge oder Teilzeichenfolge im Pfad oder in der Abfrage.

Wenn der Musterausdruck Unterausdrücke enthält (durch Klammern getrennt), wird die erste übereinstimmende Teilzeichenfolge durch die Ersatzzeichenfolge ersetzt. Wenn der Musterausdruck keine Unterausdrücke enthält, wird die gesamte übereinstimmende Zeichenfolge ersetzt.

Wenn `<expression>` leer oder nicht vorhanden ist, wird die Ersatzzeichenfolge an den Pfad oder die Abfrage angehängt.

Wenn `<substitution>` leer ist, wird die übereinstimmende Zeichenfolge oder Teilzeichenfolge entfernt. Wenn `<substitution>` nicht angegeben ist, wird der Pfad oder die Abfragezeichenfolge nicht geändert.

>[!NOTE]
>
>Alle Übereinstimmungen in der Eingabezeichenfolge werden ersetzt, wenn `replace="all"` in dem `<rule>` Element angegeben ist, zu dem dieses `<substitution>` gehört. Standardmäßig wird nur die erste Übereinstimmung durch die Ersatzzeichenfolge ersetzt.

## Notiz {#section-cedf2adabaaf441c9f598fb0ea180246}

Die Ersatzzeichenfolge darf keine literalen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` codiert werden, oder die gesamte Zeichenfolge kann in einen XML-CDATA-Abschnitt eingeschlossen werden:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
