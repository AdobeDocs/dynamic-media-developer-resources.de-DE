---
description: Musterelement für reguläre Ausdrücke. Optional in <Regel> -Elementen.
solution: Experience Manager
title: Ausdruck
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 4%

---

# Ausdruck{#expression}

Musterelement für reguläre Ausdrücke. Optional in `<rule>` -Elementen.

## Attribute {#section-fd0574eee1f9423cbb2ed709c0906800}

Keine.

## Daten {#section-4cd740c511a1432da0955e9acfbcf96f}

Musterzeichenfolge für reguläre Ausdrücke.

## Beschreibung {#section-3245c8a531bb455d8398449f6ea63b37}

Das Element `<expression>` kann leer sein oder eine einfache Suchzeichenfolge oder ein Muster für reguläre Ausdrücke enthalten. Das Muster wird auf die gesamte Anforderungszeichenfolge angewendet.

Eine Übereinstimmung tritt immer dann auf, wenn `<expression>` leer oder nicht angegeben ist. Dies entspricht der Angabe von `<expression>.*</expression>`.

Die Implementierung basiert auf dem Java-Paket [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), das eine Syntax für reguläre Ausdrücke ähnlich der von Perl bereitstellt.

## Notiz {#section-6b41a900b0ce4a9590e5861e3c81599c}

Die Zeichenfolge des Ausdrucks darf keine Zeichen &lt; und &amp; enthalten. Diese reservierten Zeichen können mit `&` und `<` kodiert werden oder die gesamte Zeichenfolge kann in einen XML `CDATA`-Abschnitt eingeschlossen werden:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle Zeichen zwischen den Tags `<expression>` und `</expression>` werden an den Parser für reguläre Ausdrücke übergeben, einschließlich Zeichen außerhalb des optionalen Abschnitts `CDATA` . Es sollte darauf geachtet werden, zusätzliche Leerzeichen zu vermeiden.

## Verwandte Themen {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
