---
description: Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze.
solution: Experience Manager
title: Befehlsmakros
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze.

Makros werden in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

Makros können an beliebiger Stelle in einer Anfrage nach dem &quot;?&quot; aufgerufen werden, ebenso an einer beliebigen Stelle in einem `catalog::Modifier` -Feld. Makros können nur einen oder mehrere vollständige Image Serving-Befehle darstellen. Daher müssen sie durch &#39;&amp;&#39;-Trennzeichen eingeschlossen sein (außer am Anfang oder Ende der Modifikatorzeichenfolge).

Makroaufrufe werden während des Parsens durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dies unterscheidet sich von `catalog::Modifier`, wobei Befehle in der Anforderungszeichenfolge Befehle in der `catalog::Modifier`-Zeichenfolge immer außer Kraft setzen, unabhängig von der Position in der Anforderung.

Makros können verschachtelt sein, mit der folgenden Einschränkung: Ein Makro kann nur aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist, indem es entweder früher in derselben Makrodefinitionsdatei erscheint oder indem die Definition für ein solches eingebettetes Makro in die Standard-Makrodefinitionsdatei aufgenommen wird.

Makros können nützlich sein, wenn dieselben Attribute auf verschiedene Bilder angewendet werden sollen.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Wir können ein Makro für die gemeinsamen Attribute definieren:

`view wid=240&fmt=pdf&imageRes=300`

Das Makro würde wie folgt verwendet:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Da `wid=` für die dritte Anforderung anders ist, überschreiben wir einfach den Wert *nach* das Makro wird aufgerufen (die Angabe `wid=`*bevor* `$view$` keine Auswirkungen hat).

+ [name](r-name.md)
