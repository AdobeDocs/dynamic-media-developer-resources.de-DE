---
title: Katalogdatendateien
description: Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (mit Ausnahme von .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (mit Ausnahme von `.ini`).

Katalogdatendateien können mithilfe von Anwendungen, die tabulatorgetrennte Textdatendateien wie Microsoft® Excel und Access unterstützen, problemlos verwaltet werden.

Eine Katalogdatendatei besteht im Wesentlichen aus einer zweidimensionalen Tabelle und einem Header-Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datensätzen werden durch einzelne `<TAB>` Zeichen getrennt. Datensätze werden durch einen einzelnen `<CR>` (ASCII-Code `0xD`), einen einzelnen `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>` -Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

In Header- und Datensätzen ist kein Leerraum außer den Trennzeichen für das Feld `<TAB>` zulässig.

In den Datensätzen zeigen zwei aufeinander folgende `<TAB>` Zeichen ein leeres Feld an. Leere Felder übernehmen Standardwerte entweder aus den Katalogattributen oder aus den Standardeinstellungen des Servers.

Datenfelder dürfen nicht die Zeichen `<CR>`, `<LF>` oder `<TAB>` enthalten, es sei denn, der Datenwert ist vom Typ Text und wird von einfachen oder doppelten Anführungszeichen eingeschlossen. Keine HTTP-Kodierung von Datenfeldern.

Wenn nicht anders angegeben, werden mehrere Datenwerte im selben Feld durch Kommas (&#39;,&#39;) getrennt.

Spalten, deren Namen mit &quot;.&quot;beginnen werden ignoriert; dies ermöglicht die Speicherung von Daten in Materialkatalogen, die für das Bild-Rendering nicht von Interesse sind. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel in derselben Datendatei mehrmals vorkommt, hat die neuere Instanz Vorrang.
