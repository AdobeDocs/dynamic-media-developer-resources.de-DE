---
description: Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (mit Ausnahme von .ini). Sie können einfach mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie z. B. Microsoft Excel und Access.
solution: Experience Manager
title: Katalogdatendateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (mit Ausnahme von .ini). Sie können einfach mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie z. B. Microsoft Excel und Access.

Eine Katalogdatendatei besteht im Wesentlichen aus einer zweidimensionalen Tabelle und einem Header-Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datensätzen werden durch einzelne `<TAB>` Zeichen getrennt. Datensätze werden durch einen einzelnen `<CR>` (ASCII-Code `0xD`), einen einzelnen `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>` -Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

Leerzeichen können nicht als Feldtrennzeichen verwendet werden. Im Header-Datensatz sind keine Leerzeichen zulässig. In Datensätzen werden Leerzeichen am Anfang oder Ende eines Datenfelds als Teil dieses Datenfelds betrachtet.

In den Datensätzen zeigen zwei aufeinander folgende `<TAB>` Zeichen ein leeres Feld an. Leere Felder können Standardwerte entweder aus den Katalogattributen oder aus den Standardeinstellungen des Servers übernehmen.

Datenfelder können optional durch doppelte Anführungszeichen eingeschlossen werden. Sie dürfen keine `<CR>`-, `<LF>`- oder `<TAB>`-Zeichen enthalten, es sei denn, der Datenwert ist vom Typ text und wird durch doppelte Anführungszeichen eingeschlossen. Datenfelder dürfen nicht HTTP-kodiert sein.

Wenn nicht anders angegeben, werden mehrere Datenwerte im selben Feld durch Kommas getrennt.

Spalten, deren Namen mit &quot;.&quot;beginnen. werden ignoriert. Dies ermöglicht das Speichern von Daten in Bildkatalogen, was für Image Serving von Interesse ist. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben und -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel in derselben Datendatei mehrmals vorkommt, hat die neuere Instanz Vorrang.
