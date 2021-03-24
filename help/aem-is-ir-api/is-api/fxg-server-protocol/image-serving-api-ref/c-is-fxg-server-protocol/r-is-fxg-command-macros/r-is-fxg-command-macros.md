---
description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.
solution: Experience Manager
title: Befehlsmakros
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Befehls-Makros{#command-macros}

Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.

Makros sind in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

Makros können an beliebiger Stelle in einer Anforderung nach dem &#39;?&#39; sowie an einer beliebigen Stelle innerhalb eines `catalog::Modifier`-Felds aufgerufen werden. Makros können nur einen oder mehrere vollständige Image Serving-Befehle darstellen. Daher müssen sie durch &quot;&amp;&quot;Trennzeichen eingeschlossen sein (außer am Anfang oder am Ende der Modifiziererzeichenfolge).

Makroaufrufe werden während der Analyse durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros setzen dieselben Befehle in der Anforderung außer Kraft, wenn sie vor dem Makroaufruf in der Anforderung auftreten. Dies unterscheidet sich von `catalog::Modifier`, wobei Befehle in der Anforderungszeichenfolge Befehle in der `catalog::Modifier`-Zeichenfolge immer außer Kraft setzen, unabhängig von der Position in der Anforderung.

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

Da `wid=` für die dritte Anforderung unterschiedlich ist, überschreiben wir einfach den Wert *nachdem* das Makro aufgerufen wurde (die Angabe `wid=`*bevor* `$view$` keine Auswirkungen hat).

+ [name](r-name.md)
