---
description: Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access.
solution: Experience Manager
title: Katalogdatendateien
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini). Sie können problemlos mit Anwendungen verwaltet werden, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access.

Eine Katalogdatendatei besteht im Wesentlichen aus einem zweidimensionalen Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datendatensätzen werden durch einzelne `<TAB>`-Zeichen getrennt. Datensätze werden durch ein einzelnes `<CR>` (ASCII-Code `0xD`), ein einzelnes `<LF>` (ASCII-Code `0xA`) oder ein `<CR><LF>`-Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

Leerzeichen können nicht als Feldtrennzeichen verwendet werden. Im Header-Datensatz sind keine Leerzeichen zulässig. In Datendatensätzen werden Leerzeichen am Anfang oder am Ende eines Datenfelds als Teil dieses Datenfelds betrachtet.

In den Datensätzen weisen zwei benachbarte `<TAB>`-Zeichen auf ein leeres Feld hin. Leere Felder übernehmen möglicherweise Standardwerte entweder aus den Katalogattributen oder aus den Standardeinstellungen des Servers.

Datenfelder können optional durch Anführungszeichen der Dublette eingeschlossen werden. Sie dürfen keine &lt; a0/>-, `<LF>`- oder `<TAB>`-Zeichen enthalten, es sei denn, der Datenwert ist vom Typ text und von Anführungszeichen für die Dublette eingeschlossen. `<CR>` Datenfelder dürfen nicht HTTP-kodiert sein.

Wenn nicht anders angegeben, werden mehrere Datenwerte im gleichen Feld durch Kommas getrennt.

Spalten, deren Namen mit &quot;&quot;Beginn werden. werden ignoriert. Dies ermöglicht die Speicherung von Daten in Bildkatalogen, was für Image Serving uninteressant ist. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Wenn derselbe Schlüssel in derselben Datendatei mehrmals vorkommt, hat die spätere Instanz Vorrang.
