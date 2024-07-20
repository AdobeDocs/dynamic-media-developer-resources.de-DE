---
title: Befehlsmakros
description: Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze. Makros werden in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze. Makros werden in separaten Makro-Definitionsdateien definiert, die an Bildkataloge oder den Standardkatalog angehängt werden können.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Makroname. </p></td> 
 </tr> 
</table>

`*`name`*` unterscheidet nicht zwischen Groß- und Kleinschreibung und kann aus einer beliebigen Kombination aus ASCII-Buchstaben, Zahlen , &#39;-&#39;, &#39;_&#39; und &#39;.&#39; bestehen. Zeichen.

Makros können an einer beliebigen Stelle in einer Anfrage nach dem &quot;?&quot;und an einer beliebigen Stelle in einem Feld `catalog::Modifier` oder `catalog::PostModifier` aufgerufen werden. Makros können nur einen oder mehrere vollständige Image Serving-Befehle darstellen und müssen mit `&` Trennzeichen von anderen Befehlen getrennt werden.

Makroaufrufe werden während des Parsens durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dieser Verarbeitungsfluss unterscheidet sich von `catalog::Modifier`, bei dem Befehle in der Anforderungszeichenfolge Befehle in der `catalog::Modifier` -Zeichenfolge immer außer Kraft setzen, unabhängig von der Position in der Anfrage.

Befehlsmakros können keine Argumentwerte haben, aber benutzerdefinierte Variablen können verwendet werden, um Werte aus der Anfrage an das Makro zu übergeben.

Makros können verschachtelt sein. Ein Makro kann jedoch nur aufgerufen werden, wenn es zum Zeitpunkt der Analyse der Makrodefinition bereits definiert ist. Dieser Workflow erfolgt entweder durch frühere Darstellung in derselben Makrodefinitionsdatei oder durch Platzieren der Definition für ein solches eingebettetes Makro in der Standard-Makrodefinitionsdatei.

## Beispiel {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Makros können nützlich sein, wenn dieselben Attribute auf verschiedene Bilder angewendet werden sollen.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Sie können ein Makro für die allgemeinen Attribute definieren:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Das Makro würde wie folgt verwendet:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Da `wid=` für die dritte Anforderung unterschiedlich ist, können Sie einfach den Wert *nach* überschreiben, wenn das Makro aufgerufen wird (die Angabe `wid=`*vor* `$view$` hat keine Auswirkungen).

## Verwandte Themen {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Macro Definition Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
