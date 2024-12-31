---
description: Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (außer .ini). Sie können problemlos mithilfe von Anwendungen gepflegt werden, die tabulatorgetrennte Textdatendateien wie Microsoft Excel und Access unterstützen.
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

Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (außer .ini). Sie können problemlos mithilfe von Anwendungen gepflegt werden, die tabulatorgetrennte Textdatendateien wie Microsoft Excel und Access unterstützen.

Eine Katalogdatendatei besteht im Wesentlichen aus einer zweidimensionalen Tabelle und einem Kopfzeilendatensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Felder sowohl in der Kopfzeile als auch in den Datensätzen werden durch einzelne `<TAB>` getrennt. Datensätze werden durch ein einzelnes `<CR>` (ASCII-Code `0xD`), ein einzelnes `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>` Paar getrennt.

Der Kopfzeilendatensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei den Namen der Datenfelder wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

Leerzeichen können nicht als Feldtrennzeichen verwendet werden. Im Kopfzeilendatensatz sind keine Leerzeichen zulässig. In Datensätzen werden alle Leerzeichen am Anfang oder Ende eines Datenfelds als Teil dieses Datenfelds betrachtet.

In den Datensätzen geben zwei benachbarte `<TAB>` ein leeres Feld an. Leere Felder können die Standardwerte entweder von den Katalogattributen oder von den Server-Standardwerten übernehmen.

Datenfelder können optional in Anführungszeichen gesetzt werden. Sie dürfen keine `<CR>`, `<LF>` oder `<TAB>` Zeichen enthalten, es sei denn, der Datenwert ist vom Typ Text und wird durch doppelte Anführungszeichen eingeschlossen. Datenfelder dürfen nicht HTTP-kodiert sein.

Mehrere Datenwerte im selben Feld werden durch Kommas getrennt, sofern nicht anders angegeben.

Spalten, deren Namen mit &quot;.“ beginnen werden ignoriert. Dies ermöglicht das Speichern von Daten in Bildkatalogen, was für Image Serving nicht von Interesse ist. Spalten mit unbekannten Kopfzeilennamen werden ignoriert und in die Protokolldatei wird eine Warnung geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie aus &quot;-&quot; und „_“ bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel mehrmals in derselben Datendatei auftritt, hat die spätere Instanz Vorrang.
