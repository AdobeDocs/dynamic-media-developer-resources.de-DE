---
description: Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie z. B. Microsoft Excel und Access.
solution: Experience Manager
title: Katalogdatendateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie z. B. Microsoft Excel und Access.

Eine Katalogdatendatei besteht im Wesentlichen aus einer zweidimensionalen Tabelle und einem Header-Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datensätzen werden durch einzelne `<TAB>` Zeichen getrennt. Datensätze werden durch einen einzelnen `<CR>` (ASCII-Code `0xD`), einen einzelnen `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>`-Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

Leerzeichen können nicht als Feldtrennzeichen verwendet werden. Im Header-Datensatz sind keine Leerzeichen zulässig. In Datensätzen werden Leerzeichen am Anfang oder Ende eines Datenfelds als Teil dieses Datenfelds betrachtet.

In den Datensätzen kennzeichnen zwei aufeinander folgende `<TAB>` Zeichen ein leeres Feld. Leere Felder können Standardwerte entweder aus den Katalogattributen oder aus den Standardeinstellungen des Servers übernehmen.

Datenfelder können optional durch doppelte Anführungszeichen eingeschlossen werden. Sie dürfen nicht die Zeichen `<CR>`, `<LF>` oder `<TAB>` enthalten, es sei denn, der Datenwert ist vom Typ Text und wird von doppelten Anführungszeichen eingeschlossen. Datenfelder dürfen nicht HTTP-kodiert sein.

Wenn nicht anders angegeben, werden mehrere Datenwerte im selben Feld durch Kommas getrennt.

Spalten, deren Namen mit &quot;.&quot;beginnen. werden ignoriert. Dies ermöglicht das Speichern von Daten in Bildkatalogen, was für Image Serving von Interesse ist. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben und -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel in derselben Datendatei mehrmals vorkommt, hat die neuere Instanz Vorrang.
