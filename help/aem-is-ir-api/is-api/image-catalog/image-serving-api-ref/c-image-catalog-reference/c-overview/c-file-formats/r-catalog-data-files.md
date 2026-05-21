---
description: Katalogdatendateien können einen beliebigen Namen und ein beliebiges Dateisuffix aufweisen (außer .ini). Sie können problemlos mithilfe von Anwendungen gepflegt werden, die tabulatorgetrennte Textdatendateien wie Microsoft Excel und Access unterstützen.
solution: Experience Manager
title: Katalogdatendateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
TQID: 'https://experienceleague.adobe.com/h4-MIosWMEWhmbAYbpS9xm22nDzEPO6APGEezCA1B-Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 353
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
