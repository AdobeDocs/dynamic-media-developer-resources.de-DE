---
description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit. Makros sind in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.
seo-description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit. Makros sind in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.
seo-title: Befehlsmakros
solution: Experience Manager
title: Befehlsmakros
uuid: a6ff5642-6716-484f-b37e-066994362a9b
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# Befehls-Makros{#command-macros}

Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit. Makros sind in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Makroname. </p></td> 
 </tr> 
</table>

`*`Bei `*` Namen wird nicht zwischen Groß- und Kleinschreibung unterschieden und es kann sich um eine beliebige Kombination aus ASCII-Buchstaben, -Zahlen, -Zeichen, -Zeichen, -Zeichen und -Zeichen handeln. Zeichen.

Makros können an einer beliebigen Stelle in einer Anforderung nach dem &quot;?&quot;aufgerufen werden, ebenso an einer beliebigen Stelle innerhalb eines Felds `catalog::Modifier` oder `catalog::PostModifier`. Makros können nur einen oder mehrere vollständige Image Serving-Befehle darstellen und müssen von anderen Befehlen mit &quot;&amp;&quot;Trennzeichen getrennt werden.

Makroaufrufe werden während der Analyse durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros setzen dieselben Befehle in der Anforderung außer Kraft, wenn sie vor dem Makroaufruf in der Anforderung auftreten. Dies unterscheidet sich von `catalog::Modifier`, wobei Befehle in der Anforderungszeichenfolge Befehle in der `catalog::Modifier`-Zeichenfolge immer außer Kraft setzen, unabhängig von der Position in der Anforderung.

Befehlsmakros können keine Argumentwerte haben, aber benutzerdefinierte Variablen können verwendet werden, um Werte aus der Anforderung an das Makro zu übergeben.

Makros können verschachtelt sein, mit der folgenden Einschränkung: Ein Makro kann nur dann aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist, entweder indem es früher in derselben Makrodefinitionsdatei angezeigt wird oder indem die Definition für ein solches eingebettetes Makro in der Standarddatei für die Makrodefinition platziert wird.

## Beispiel {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Makros können nützlich sein, wenn dieselben Attribute auf verschiedene Bilder angewendet werden sollen.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Wir können ein Makro für die allgemeinen Attribute definieren:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Das Makro wird wie folgt verwendet:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Da `wid=` für die dritte Anforderung unterschiedlich ist, überschreiben wir einfach den Wert *nachdem* das Makro aufgerufen wurde (die Angabe `wid=`*bevor* `$view$` keine Auswirkungen hat).

## Verwandte Themen {#section-8cdba0ed2480444ca61e719e54f8871c}

[Katalog::MakroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [Katalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md),  [Makro-Definitionsreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
