---
description: Musterelement für reguläre Ausdrücke. Optional in <rule>-Elementen.
solution: Experience Manager
title: Ausdruck
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# Ausdruck{#expression}

Musterelement für reguläre Ausdrücke. Optional in `<rule>`.

## Attribute {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Keine.

## Daten {#section-e2601008d71243109af1a8c55b58416d}

Zeichenfolge für Muster regulärer Ausdrücke.

## Beschreibung {#section-759bfb738ddb45dba1f0807aba8c1113}

Das `<expression>` kann leer sein oder eine einfache Suchzeichenfolge oder ein Muster für reguläre Ausdrücke enthalten. Das Muster wird auf die gesamte Anforderungszeichenfolge angewendet.

Eine Übereinstimmung tritt immer dann auf, wenn `<expression>` leer oder nicht angegeben ist. Dies entspricht der Angabe von `<expression>.*</expression>`.

Die Implementierung basiert auf dem Java-Paket [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), das eine Syntax regulärer Ausdrücke ähnlich der von Perl bereitstellt.

## Anmerkungen {#section-10b472a902674893b49ca49a7052c366}

Die Ausdruckszeichenfolge darf keine literalen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` codiert werden, oder die gesamte Zeichenfolge kann in einen XML-`CDATA`-Abschnitt eingeschlossen werden:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle Zeichen zwischen den Tags `<expression>` und `</expression>` werden an den Parser für reguläre Ausdrücke übergeben, einschließlich der Zeichen außerhalb des optionalen `CDATA`. Es sollte darauf geachtet werden, dass keine zusätzlichen Leerzeichen entstehen.

## Verwandte Themen {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
