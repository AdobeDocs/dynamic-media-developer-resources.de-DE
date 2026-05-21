---
title: Befehlsmakros
description: Befehlsmakros bieten benannte Tastaturbefehle für Befehlssätze.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
TQID: 'https://experienceleague.adobe.com/DbXn35KC7OLFI0Dulgobj3UFPHnubmCisNDS541j8lE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 248
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten benannte Tastaturbefehle für Befehlssätze.

Makros werden in separaten Makrodefinitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

Makros können in einer Anfrage an einer beliebigen Stelle nach dem &quot;?“ und an einer beliebigen Stelle in einem `catalog::Modifier` aufgerufen werden. Makros können nur einen oder mehrere vollständige Bildbereitstellungsbefehle darstellen, daher müssen sie von &quot;&amp;&quot;-Trennzeichen eingeschlossen werden (außer wenn am Anfang oder Ende der Modifikatorzeichenfolge steht).

Makroaufrufe werden durch ihre Ersatzzeichenfolgen frühzeitig während der Analyse ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dieser Fluss unterscheidet sich von `catalog::Modifier`, bei dem Befehle in der Anfragezeichenfolge unabhängig von der Position in der Anfrage immer Befehle in der `catalog::Modifier` überschreiben.

Makros können verschachtelt werden. Ein Makro kann jedoch nur aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist. Dieser Fluss wird erreicht, indem entweder zuvor in derselben Makrodefinitionsdatei angezeigt wird oder indem die Definition für ein solches eingebettetes Makro in der standardmäßigen Makrodefinitionsdatei platziert wird.

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

Da `wid=` für die dritte Anfrage anders ist, überschreiben Sie einfach den Wert *nachdem* das Makro aufgerufen wurde (die Angabe von `wid=` *vorher* `$view$` hat keine Auswirkung).

+ [name](r-name.md)
