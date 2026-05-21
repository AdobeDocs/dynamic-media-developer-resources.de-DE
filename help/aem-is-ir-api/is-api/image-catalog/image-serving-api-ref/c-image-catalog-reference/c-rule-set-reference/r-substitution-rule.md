---
description: Ersatz-Zeichenfolgenelement. Optional in <rule>-Elementen.
solution: Experience Manager
title: Substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
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
