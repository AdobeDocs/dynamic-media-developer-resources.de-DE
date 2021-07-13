---
description: Ersatzzeichenfolgen-Element. Optional in <Regel> -Elementen.
solution: Experience Manager
title: Substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# Substitution{#substitution}

Ersatzzeichenfolgen-Element. Optional in `<rule>` -Elementen.

## Attribute {#section-d955eefc53eb4274861270669c01f9ca}

Keine.

## Daten {#section-a2688866ed6d41279a8478886e511ae3}

Ersatzzeichenfolge.

## Beschreibung {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definiert eine Ersatzzeichenfolge für die übereinstimmende Zeichenfolge oder Unterzeichenfolge im Pfad oder in der Abfrage.

Wenn der Musterausdruck Unterausdrücke enthält (durch Klammern getrennt), wird die erste übereinstimmende Unterzeichenfolge durch die Ersatzzeichenfolge ersetzt. Wenn der Musterausdruck keine Unterausdrücke enthält, wird die gesamte übereinstimmende Zeichenfolge ersetzt.

Wenn `<expression>` leer oder fehlt, wird die Ersatzzeichenfolge an den Pfad oder die Abfrage angehängt.

Wenn `<substitution>` leer ist, wird die übereinstimmende Zeichenfolge oder Unterzeichenfolge entfernt. Wenn `<substitution>` nicht angegeben ist, wird der Pfad oder die Abfragezeichenfolge nicht geändert.

## Notiz {#section-90fe89bb17a04804b7ff3c93df082892}

Die Ersatzzeichenfolge darf keine &lt;- und &amp;-Zeichen in Textform enthalten. Diese reservierten Zeichen können mit `&` und `<` kodiert werden oder die gesamte Zeichenfolge kann in einen XML `CDATA`-Abschnitt eingeschlossen werden:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
