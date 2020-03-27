---
description: Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access.
seo-description: Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access.
seo-title: Katalogdatendateien
solution: Experience Manager
title: Katalogdatendateien
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access.

Eine Katalogdatendatei besteht im Wesentlichen aus einem zweidimensionalen Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datensätzen werden durch einzelne `<TAB>` Zeichen getrennt. Datensätze werden durch einen einzelnen `<CR>` (ASCII-Code `0xD`), einen einzelnen `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>` Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

Leerzeichen können nicht als Feldtrennzeichen verwendet werden. Im Header-Datensatz sind keine Leerzeichen zulässig. In Datendatensätzen werden Leerzeichen am Anfang oder am Ende eines Datenfelds als Teil dieses Datenfelds betrachtet.

In den Datendatensätzen gibt es zwei benachbarte `<TAB>` Zeichen, die auf ein leeres Feld hinweisen. Leere Felder übernehmen möglicherweise Standardwerte entweder aus den Katalogattributen oder aus den Standardeinstellungen des Servers.

Datenfelder können optional durch Anführungszeichen der Dublette eingeschlossen werden. Sie dürfen keine `<CR>`, `<LF>`oder `<TAB>` Zeichen enthalten, es sei denn, der Datenwert ist vom Typ text und von Anführungszeichen der Dublette eingeschlossen. Datenfelder dürfen nicht HTTP-kodiert sein.

Wenn nicht anders angegeben, werden mehrere Datenwerte im gleichen Feld durch Kommas getrennt.

Spalten, deren Namen mit &quot;&quot;Beginn werden. werden ignoriert. Dies ermöglicht die Speicherung von Daten in Bildkatalogen, was für Image Serving uninteressant ist. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel in derselben Datendatei mehrmals vorkommt, hat die spätere Instanz Vorrang.
