---
description: Musterelement für reguläre Ausdrücke. Optional in <rule>-Elementen.
solution: Experience Manager
title: Ausdruck
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
TQID: 'https://experienceleague.adobe.com/zMAFfzeypXmMIx1aO1xmHdF-UkHJPHKp7KUgi05F94w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 3%

---

# Ausdruck{#expression}

Musterelement für reguläre Ausdrücke. Optional in `<rule>`.

## Attribute {#section-fd0574eee1f9423cbb2ed709c0906800}

Keine.

## Daten {#section-4cd740c511a1432da0955e9acfbcf96f}

Zeichenfolge für Muster regulärer Ausdrücke.

## Beschreibung {#section-3245c8a531bb455d8398449f6ea63b37}

Das `<expression>` kann leer sein oder eine einfache Suchzeichenfolge oder ein Muster für reguläre Ausdrücke enthalten. Das Muster wird auf die gesamte Anforderungszeichenfolge angewendet.

Eine Übereinstimmung tritt immer dann auf, wenn `<expression>` leer oder nicht angegeben ist. Dies entspricht der Angabe von `<expression>.*</expression>`.

Die Implementierung basiert auf dem Java-Paket [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e) das eine Syntax für reguläre Ausdrücke ähnlich der von Perl bereitstellt.

## Notiz {#section-6b41a900b0ce4a9590e5861e3c81599c}

Die Ausdruckszeichenfolge darf keine literalen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` codiert werden, oder die gesamte Zeichenfolge kann in einen XML-`CDATA`-Abschnitt eingeschlossen werden:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle Zeichen zwischen den Tags `<expression>` und `</expression>` werden an den Parser für reguläre Ausdrücke übergeben, einschließlich der Zeichen außerhalb des optionalen `CDATA`. Es sollte darauf geachtet werden, dass keine zusätzlichen Leerzeichen entstehen.

## Verwandte Themen {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
