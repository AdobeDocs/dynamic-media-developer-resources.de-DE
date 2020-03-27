---
description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.
seo-description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.
seo-title: Befehlsmakros
solution: Experience Manager
title: Befehlsmakros
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b

---


# Befehlsmakros{#command-macros}

Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.

Makros sind in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

Makros können an beliebiger Stelle in einer Anforderung nach dem &#39;?&#39; sowie an einer beliebigen Stelle innerhalb eines `catalog::Modifier` Felds aufgerufen werden. Makros können nur einen oder mehrere vollständige Image Serving-Befehle darstellen. Daher müssen sie durch &quot;&amp;&quot;Trennzeichen eingeschlossen sein (außer am Anfang oder am Ende der Modifiziererzeichenfolge).

Makroaufrufe werden während der Analyse durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros setzen dieselben Befehle in der Anforderung außer Kraft, wenn sie vor dem Makroaufruf in der Anforderung auftreten. Dies unterscheidet sich von `catalog::Modifier`dem, dass Befehle in der Anforderungszeichenfolge Befehle in der `catalog::Modifier` Zeichenfolge immer außer Kraft setzen, unabhängig von der Position in der Anforderung.

Makros können verschachtelt sein, mit der folgenden Einschränkung: Ein Makro kann nur dann aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist, entweder indem es früher in derselben Makrodefinitionsdatei angezeigt wird oder indem die Definition für ein solches eingebettetes Makro in die Standarddatei für die Makrodefinition eingefügt wird.

Makros können nützlich sein, wenn dieselben Attribute auf verschiedene Bilder angewendet werden sollen.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Wir können ein Makro für die allgemeinen Attribute definieren:

`view wid=240&fmt=pdf&imageRes=300`

Das Makro wird wie folgt verwendet:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Da die dritte Anforderung unterschiedlich `wid=` ist, überschreiben wir den Wert einfach, *nachdem* das Makro aufgerufen wurde (die Angabe `wid=`*vor *`$view$`dem Aufruf hätte keine Auswirkungen).

+ [name](r-name.md)
