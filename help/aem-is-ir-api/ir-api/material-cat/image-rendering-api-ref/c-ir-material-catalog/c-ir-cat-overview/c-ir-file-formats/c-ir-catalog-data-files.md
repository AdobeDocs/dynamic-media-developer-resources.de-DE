---
description: Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini).
solution: Experience Manager
title: Katalogdatendateien
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Katalogdatendateien{#catalog-data-files}

Katalogdatendateien können einen beliebigen Namen und Dateisuffix haben (mit Ausnahme von .ini).

Katalogdatendateien können mithilfe von Anwendungen, die tabulatorgetrennte Textdatendateien unterstützen, wie Microsoft Excel und Access, problemlos verwaltet werden.

Eine Katalogdatendatei besteht im Wesentlichen aus einem zweidimensionalen Datensatz, der die Datenspalten und eine beliebige Anzahl von Datensätzen (Zeilen) identifiziert. Die Felder in der Kopfzeile und in den Datendatensätzen werden durch einzelne `<TAB>`-Zeichen getrennt. Datensätze werden durch ein einzelnes `<CR>` (ASCII-Code 0xD), ein einzelnes `<LF>` (ASCII-Code 0xA) oder ein `<CR><LF>`-Paar getrennt.

Der Header-Datensatz muss die genauen Namen für jedes Datenfeld enthalten. Leere Felder sind in der Kopfzeile nicht zulässig. Bei Datenfeldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Alle Feldnamen müssen eindeutig sein.

In Header- und Datendatensätzen ist kein Leerraum außer den Feldtrennzeichen `<TAB>` zulässig.

In den Datensätzen weisen zwei benachbarte `<TAB>`-Zeichen auf ein leeres Feld hin. Leere Felder übernehmen Standardwerte entweder aus den Katalogattributen oder aus den Serverstandardwerten.

Datenfelder dürfen keine Zeichen von &quot;`<CR>`&quot;, &quot;`<LF>`&quot;oder &quot;`<TAB>`&quot;enthalten, es sei denn, der Datenwert ist vom Typ &quot;text&quot;und von einfachen oder Dubletten-Anführungszeichen eingeschlossen. Datenfelder dürfen nicht HTTP-kodiert sein.

Wenn nicht anders angegeben, werden mehrere Datenwerte im gleichen Feld durch Kommas (&#39;,&#39;) getrennt.

Spalten, deren Namen mit &#39;&#39; Beginn werden. werden ignoriert; Dies ermöglicht die Speicherung von Daten in Materialkatalogen, die für das Image Rendering uninteressant sind. Spalten mit unbekannten Header-Namen werden ignoriert und eine Warnung in die Protokolldatei geschrieben.

Feldnamen können aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen sowie &quot;-&quot;und &quot;_&quot;bestehen.

Eine oder mehrere Spalten können als Indexschlüssel verwendet werden. Tritt der gleiche Schlüssel mehr als einmal in derselben Datendatei auf, hat die spätere Instanz Vorrang.
