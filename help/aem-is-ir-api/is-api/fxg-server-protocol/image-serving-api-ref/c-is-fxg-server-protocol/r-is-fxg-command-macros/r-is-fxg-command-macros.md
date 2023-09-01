---
title: Befehlsmakros
description: Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze.

Makros werden in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

Makros können an einer beliebigen Stelle in einer Anfrage nach dem &quot;?&quot;und an einer beliebigen Stelle in einer `catalog::Modifier` -Feld. Makros können nur einen oder mehrere vollständige Image Serving-Befehle darstellen. Daher muss sie durch &#39;&amp;&#39;-Trennzeichen eingeschlossen sein (außer am Anfang oder Ende der Modifikatorzeichenfolge).

Makroaufrufe werden während des Parsens durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dieser Fluss unterscheidet sich von `catalog::Modifier`, wobei Befehle in der Anfragezeichenfolge Befehle in der `catalog::Modifier` Zeichenfolge, unabhängig von der Position in der Anforderung.

Makros können verschachtelt werden. Ein Makro kann jedoch nur aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist. Dieser Ablauf erfolgt entweder durch frühere Darstellung in derselben Makrodefinitionsdatei oder durch Platzieren der Definition für ein solches eingebettetes Makro in der Standarddatei für die Makrodefinition.

Makros können nützlich sein, wenn dieselben Attribute auf verschiedene Bilder angewendet werden sollen.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

Sie können ein Makro für die allgemeinen Attribute definieren:

`view wid=240&fmt=pdf&imageRes=300`

Das Makro würde wie folgt verwendet:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

weil `wid=` unterscheidet sich bei der dritten Anforderung, überschreiben Sie einfach den Wert *after* das Makro aufgerufen wird (Angabe von `wid=` *before* `$view$` keine Wirkung hat).

+ [name](r-name.md)
