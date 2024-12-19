---
title: Befehlsmakros
description: Befehlsmakros bieten benannte Tastaturbefehle für Befehlssätze. Makros werden in separaten Makrodefinitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten benannte Tastaturbefehle für Befehlssätze. Makros werden in separaten Makrodefinitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Name</span></span> </p> </td> 
  <td class="stentry"> <p>Makroname. </p></td> 
 </tr> 
</table>

`*`name`*` unterscheidet nicht zwischen Groß- und Kleinschreibung und kann aus einer beliebigen Kombination von ASCII-Buchstaben, Zahlen , &#39;-&#39;, &#39;_&#39; und &#39;.&#39; bestehen. Zeichen.

Makros können in einer Anfrage an einer beliebigen Stelle nach dem &quot;?“ und an einer beliebigen Stelle innerhalb eines `catalog::Modifier`- oder `catalog::PostModifier` aufgerufen werden. Makros können nur einen oder mehrere vollständige Image-Serving-Befehle darstellen und müssen von anderen Befehlen durch `&` Trennzeichen getrennt werden.

Makroaufrufe werden durch ihre Ersatzzeichenfolgen frühzeitig während der Analyse ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dieser Verarbeitungsfluss unterscheidet sich von `catalog::Modifier`, bei dem Befehle in der Anfragezeichenfolge unabhängig von der Position in der Anfrage immer Befehle in der `catalog::Modifier` überschreiben.

Befehlsmakros dürfen keine Argumentwerte enthalten, jedoch können benutzerdefinierte Variablen verwendet werden, um Werte aus der Anforderung an das Makro zu übergeben.

Makros können verschachtelt sein. Ein Makro kann jedoch nur aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist. Dieser Workflow erfolgt entweder, indem er zuvor in derselben Makrodefinitionsdatei angezeigt wird, oder indem die Definition für ein solches eingebettetes Makro in die standardmäßige Makrodefinitionsdatei eingefügt wird.

## Beispiel {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Makros können nützlich sein, wenn dieselben Attribute auf verschiedene Bilder angewendet werden sollen.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Sie können ein Makro für die allgemeinen Attribute definieren:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Das Makro würde wie folgt verwendet:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Da `wid=` für die dritte Anfrage anders ist, können Sie einfach den Wert überschreiben *nachdem* das Makro aufgerufen wurde (die Angabe von `wid=`*vorher* hat `$view$` Wirkung).

## Verwandte Themen {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)Modifier, [Referenz für Makrodefinitionen](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
