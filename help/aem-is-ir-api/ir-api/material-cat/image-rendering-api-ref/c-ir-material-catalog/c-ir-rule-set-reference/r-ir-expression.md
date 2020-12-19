---
description: Musterelement "Regulärer Ausdruck". Optional in <rule>-Elementen.
seo-description: Musterelement "Regulärer Ausdruck". Optional in <rule>-Elementen.
seo-title: ausdruck
solution: Experience Manager
title: ausdruck
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 4%

---


# ausdruck{#expression}

Musterelement &quot;Regulärer Ausdruck&quot;. Optional in `<rule>`-Elementen.

## Attribute {#section-fd0574eee1f9423cbb2ed709c0906800}

Keine.

## Daten {#section-4cd740c511a1432da0955e9acfbcf96f}

Musterzeichenfolge für regulären Ausdruck.

## Beschreibung {#section-3245c8a531bb455d8398449f6ea63b37}

Das `<expression>`-Element kann leer sein oder eine einfache Suchzeichenfolge oder ein reguläres Ausdruck-Muster enthalten. Das Muster wird auf die gesamte Anforderungszeichenfolge angewendet.

Eine Übereinstimmung tritt immer dann ein, wenn `<expression>` leer ist oder nicht angegeben ist. entspricht der Angabe von `<expression>.*</expression>`.

Die Implementierung basiert auf dem Java-Paket [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), das eine Syntax für reguläre Ausdruck wie die von Perl bereitstellt.

## Hinweis {#section-6b41a900b0ce4a9590e5861e3c81599c}

Die Zeichenfolge für Ausdruck darf keine wörtlichen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` kodiert werden, oder die gesamte Zeichenfolge kann in einen XML `CDATA`-Abschnitt eingeschlossen werden:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle Zeichen zwischen den Tags `<expression>` und `</expression>` werden an den Parser des regulären Ausdrucks übergeben, einschließlich Zeichen außerhalb des optionalen Abschnitts `CDATA`. Es sollte darauf geachtet werden, dass keine zusätzlichen Leerzeichen verwendet werden.

## Verwandte Themen {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
