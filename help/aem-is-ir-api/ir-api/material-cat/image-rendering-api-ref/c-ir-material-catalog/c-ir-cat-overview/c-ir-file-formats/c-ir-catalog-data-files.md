---
title: Katalogdatendateien
description: Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (außer .ini).
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

Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (außer `.ini`).

Katalogdatendateien können problemlos mithilfe von Anwendungen gepflegt werden, die tabulatorgetrennte Textdatendateien unterstützen, z. B. Microsoft® Excel und Access.

Im Wesentlichen eine zweidimensionale Tabelle, besteht eine Katalogdatendatei aus einem Header-Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Felder sowohl in der Kopfzeile als auch in den Datensätzen werden durch einzelne `<TAB>` getrennt. Datensätze werden durch ein einzelnes `<CR>` (ASCII-Code `0xD`), ein einzelnes `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>` Paar getrennt.

Der Kopfzeilendatensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei den Namen der Datenfelder wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

Außer den `<TAB>` Feldtrennzeichen ist in Kopfzeilen- und Datensätzen kein Leerraum zulässig.

In den Datensätzen geben zwei benachbarte `<TAB>` ein leeres Feld an. Leere Felder übernehmen Standardwerte entweder aus den Katalogattributen oder aus den Server-Standardwerten.

Datenfelder dürfen keine `<CR>`, `<LF>` oder `<TAB>` Zeichen enthalten, es sei denn, der Datenwert ist vom Typ Text und wird durch einfache oder doppelte Anführungszeichen eingeschlossen. Datenfelder nicht HTTP-kodieren.

Mehrere Datenwerte im selben Feld werden durch Kommas (&#39;,&#39;) getrennt, sofern nicht anders angegeben.

Spalten, deren Namen mit &quot;.“ beginnen werden ignoriert; dies ermöglicht das Speichern von Daten in Materialkatalogen, die für das Bild-Rendering nicht von Interesse sind. Spalten mit unbekannten Kopfzeilennamen werden ignoriert und in die Protokolldatei wird eine Warnung geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen und &quot;-&quot; und „_“ bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel mehrmals in derselben Datendatei auftritt, hat die spätere Instanz Vorrang.
