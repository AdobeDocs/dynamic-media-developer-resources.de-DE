---
description: Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini).
seo-description: Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini).
seo-title: Katalogdatendateien
solution: Experience Manager
title: Katalogdatendateien
topic: Scene7 Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini).

Katalogdatendateien können mithilfe von Anwendungen, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access, problemlos verwaltet werden.

Eine Katalogdatendatei besteht im Wesentlichen aus einem zweidimensionalen Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datensätzen werden durch einzelne `<TAB>` Zeichen getrennt. Datensätze werden durch ein einzelnes `<CR>` (ASCII-Code 0xD), ein einzelnes `<LF>` (ASCII-Code 0xA) oder ein `<CR><LF>` Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

In Header- und Datendatensätzen ist kein Leerraum außer den `<TAB>` Feldtrennzeichen zulässig.

In den Datendatensätzen gibt es zwei benachbarte `<TAB>` Zeichen, die auf ein leeres Feld hinweisen. Leere Felder übernehmen Standardwerte entweder aus den Katalogattributen oder aus den Serverstandardwerten.

Datenfelder dürfen keine `<CR>`, `<LF>`oder `<TAB>` Zeichen enthalten, es sei denn, der Datenwert ist vom Typ text und von einfachen oder Dubletten-Anführungszeichen eingeschlossen. Datenfelder dürfen nicht HTTP-kodiert sein.

Wenn nicht anders angegeben, werden mehrere Datenwerte im gleichen Feld durch Kommas (&#39;,&#39;) getrennt.

Spalten, deren Namen mit &#39;&#39; Beginn werden. werden ignoriert; Dies ermöglicht die Speicherung von Daten in Materialkatalogen, die für das Image Rendering uninteressant sind. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Tritt der gleiche Schlüssel mehr als einmal in derselben Datendatei auf, ist die spätere Instanz gültig.
