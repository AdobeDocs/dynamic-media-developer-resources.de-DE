---
description: Reguläres Musterelement für Ausdruck. Optional in <rule>-Elementen.
solution: Experience Manager
title: Ausdruck
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 4%

---


# Ausdruck{#expression}

Reguläres Musterelement für Ausdruck. Optional in `<rule>`-Elementen.

## Attribute {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Keine.

## Daten {#section-e2601008d71243109af1a8c55b58416d}

Musterzeichenfolge für regulären Ausdruck.

## Beschreibung {#section-759bfb738ddb45dba1f0807aba8c1113}

Das `<expression>`-Element kann leer sein oder eine einfache Suchzeichenfolge oder ein reguläres Ausdruck-Muster enthalten. Das Muster wird auf die gesamte Anforderungszeichenfolge angewendet.

Eine Übereinstimmung tritt immer dann ein, wenn `<expression>` leer ist oder nicht angegeben ist. entspricht der Angabe von `<expression>.*</expression>`.

Die Implementierung basiert auf dem Java-Paket [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), das eine ähnliche Syntax für reguläre Ausdruck wie Perl bereitstellt.

## Anmerkungen {#section-10b472a902674893b49ca49a7052c366}

Die Zeichenfolge für Ausdruck darf keine wörtlichen &lt;- und &amp;-Zeichen enthalten. Diese reservierten Zeichen können mit `&` bzw. `<` kodiert werden, oder die gesamte Zeichenfolge kann in einen XML `CDATA`-Abschnitt eingeschlossen werden:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alle Zeichen zwischen den Tags `<expression>` und `</expression>` werden an den Parser des regulären Ausdrucks übergeben, einschließlich Zeichen außerhalb des optionalen Abschnitts `CDATA`. Es sollte darauf geachtet werden, dass keine zusätzlichen Leerzeichen verwendet werden.

## Verwandte Themen {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
