---
description: Substitutionsvariablen werden verwendet, um Werte aus der Anforderungs-URL in in Bildkatalogen gespeicherte Vorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anforderung zu verteilen.
seo-description: Substitutionsvariablen werden verwendet, um Werte aus der Anforderungs-URL in in Bildkatalogen gespeicherte Vorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anforderung zu verteilen.
seo-title: Substitutionsvariablen
solution: Experience Manager
title: Substitutionsvariablen
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Substitutionsvariablen{#substitution-variables}

Substitutionsvariablen werden verwendet, um Werte aus der Anforderungs-URL in in Bildkatalogen gespeicherte Vorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anforderung zu verteilen.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Variablenname. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable festgelegt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

Variablendefinitionen und -verweise können im Bereich der Abfrage der Anforderung, in `catalog::Modifier` und in `catalog::PostModifier` auftreten.

Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle. der führende &#39;$&#39; identifiziert den Befehl als Variablendefinition. Variablen müssen definiert werden, bevor sie referenziert werden.

Bei dem Variablennamen *`var`* wird nicht zwischen Groß- und Kleinschreibung unterschieden und es kann sich um eine beliebige Kombination aus ASCII-Buchstaben, -Zahlen, -Zeichen, -Zeichen, -Zeichen und -Zeichen handeln.

>[!NOTE]
>
>*`value`* muss für eine sichere HTTP-Übertragung mit einem Pass URL-kodiert sein. Dublette-Codierung ist erforderlich, wenn *`value`* über HTTP erneut übertragen wird. Dies ist der Fall, wenn *`value`* in eine verschachtelte ausländische Anforderung oder in das href-Attribut eines SVG `<image>`-Elements ersetzt wird.

Variablenreferenzen bestehen aus dem Variablennamen, der durch das vorangestellte und nachfolgende &#39;$&#39; ($*var*$) getrennt wird. Verweise können an einer beliebigen Stelle im Wertebereich von IS-Befehlen auftreten (d. h. zwischen dem &#39;=&#39; nach dem Befehlsnamen und dem nachfolgenden &#39;&amp;&#39; oder dem Ende der Anforderung). Benutzerdefinierte Variablen können nicht auf die Befehle `layer=` und `effect=` angewendet werden. Im selben Befehlswert sind mehrere Variablen zulässig. Der Server ersetzt jedes Vorkommen von ` $ *`var`*$` durch *`value`*.

Variablenverweise sind möglicherweise nicht verschachtelt. Vorkommnisse von ` $ *`var`*$` innerhalb von *`value`* werden nicht ersetzt.

Beispielsweise das Anforderungsfragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

löst Folgendes auf:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; ist kein reserviertes Zeichen; es kann andernfalls in der Anforderung auftreten. Beispiel: `src=my$image$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Katalogeintrag oder eine Bilddatei mit dem Namen `my$image$file.tif` vorhanden ist), `wid=$number$` nicht, da `wid` ein numerisches Argument erfordert.

## Variablenverarbeitung in verschachtelten Anforderungen {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *``*$` Variablenverweise können an einer beliebigen Stelle innerhalb der geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben dem &quot;?&quot;. Trennen des Pfads von der Abfrage. Der Server ersetzt diese Referenzen durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anforderung weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle ` $ *`var`*=`-Definitionen aus der URL oder `catalog::Modifier` an alle verschachtelten Image Serving- und Image Rendering-Anforderungen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen unabhängig von der Verschachtelungsebene für alle Vorlagen verfügbar sind.

Unabhängig von der Verschachtelungsstufe muss nur eine HTTP-Kodierung mit einem Durchgang auf Variablenwerte angewendet werden, die an einer beliebigen Stelle in verschachtelten Image Rendering- oder Image Serving-Anforderungen oder den zugehörigen `catalog::Modifier`-Zeichenfolgen ersetzt werden sollen.

## Variablenverarbeitung in eingebetteten ausländischen Anforderungen {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *``*$` Varreferenzen, die an einer beliebigen Stelle innerhalb der geschweiften Klammern einer eingebetteten Fremdanforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt. Dadurch können eingebettete ausländische Anforderungen in eine Vorlage in einem Bildkatalog eingefügt werden.

Variablenwerte, die in fremde Anfragen ersetzt werden sollen, müssen in der Regel mit Dubletten kodiert werden, da keine Neukodierung angewendet wird, bevor der Server versucht, die finale ausländische URL zu übertragen.

## Variablenverarbeitung in SVG-Dateien {#section-a8359f9909764142b6a18ae778dca913}

` $ *`In SVG-Dateien können `*$` Variablenverweise in Attributwerten und in  `<text>` Zeichenfolgen auftreten. Image Serving ersetzt diese durch die entsprechenden ` $ *`var`*=`-Definitionen, die auf der Anforderungsverschachtelungsebene, auf der die SVG-Datei angegeben ist, bekannt sind.

>[!NOTE]
>
>Jeder Variablenwert, der in einen `href`-Attributwert ersetzt werden soll, muss URL-kodiert für die Dublette sein. alle anderen müssen einzeln kodiert sein.

## Vordefinierte Pfadvariable {#section-930d0dd12e8f49499becc9fe8df24092}

Das im Anforderungspfad angegebene *`object`* wird der vordefinierten Variablen ` *`$object`*` zugewiesen. &#39; ` $ *`object`*$`&#39; kann an einer beliebigen Stelle in der Anforderung platziert werden, in der Vorlage, auf die die Anforderung verweist, oder in einer verschachtelten/eingebetteten Anforderung, in der ein solches Objekt zulässig ist, einschließlich des Werts `src=` und `mask=` sowie des Pfads einer verschachtelten/eingebetteten Anforderung.

Beispielsweise wird in der folgenden Anforderung das im Pfad angegebene Bild als Quelle einer Ebene in einer verschachtelten Anforderung wiederverwendet:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Dies entspricht

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

Die Definition von ` *`$object`*` kann überschrieben werden, indem ` $ *`object`*=` explizit mit dem gewünschten Wert angegeben wird.

Die vordefinierte Pfadvariable wird häufig zusammen mit `template=` verwendet.

## Standard {#section-b02483d15529444586a2e9504805b155}

Keine. Nur definierte Variablen werden vom Server ersetzt (mit Ausnahme der vordefinierten Pfadvariablen $object, die immer ersetzt werden). Vorkommnisse von ` $ *`var`*$` bleiben literal, wenn ` *`var`*`nicht mit einer vorhandenen Variablendefinition übereinstimmen kann.

## Beispiele {#section-fba9393df6984247b7e30b3f93992e86}

Siehe &quot;Beispiel A&quot;in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
