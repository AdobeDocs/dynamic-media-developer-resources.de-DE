---
description: Substitutionsvariablen werden verwendet, um Werte von der Anfrage-URL zu in Bildkatalogen gespeicherten Compositing-Vorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anfrage zu übermitteln.
solution: Experience Manager
title: Substitutionsvariablen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Substitutionsvariablen{#substitution-variables}

Substitutionsvariablen werden verwendet, um Werte von der Anfrage-URL zu in Bildkatalogen gespeicherten Compositing-Vorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anfrage zu übermitteln.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variablenname. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable gesetzt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

Variablendefinitionen und -verweise können im Abfrageteil der Anfrage, in `catalog::Modifier` und in `catalog::PostModifier` vorkommen.

Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle. Das führende &quot;$&quot; identifiziert den Befehl als eine Variablendefinition. Variablen müssen definiert werden, bevor sie referenziert werden.

Beim Variablennamen *`var`* wird nicht zwischen Groß- und Kleinschreibung unterschieden. Er kann aus einer beliebigen Kombination von ASCII-Buchstaben, Zahlen, &#39;-&#39;, &#39;_&#39; und &#39;.&#39; bestehen.

>[!NOTE]
>
>*`value`* muss für eine sichere HTTP-Übertragung URL-kodiert sein. Bei einer erneuten Übertragung von *`value`* über HTTP ist eine doppelte Kodierung erforderlich. Dies ist der Fall, wenn *`value`* in eine verschachtelte Fremdanforderung oder in das href-Attribut eines SVG-`<image>` ersetzt wird.

Variablenverweise bestehen aus dem Variablennamen, der durch &quot;$&quot; ($*var*$) am Anfang und Ende getrennt ist. Verweise können an jeder beliebigen Stelle im Wertteil eines beliebigen IS-Befehls auftreten (d. h. zwischen dem &quot;=&quot;, das dem Befehlsnamen folgt, und dem nachfolgenden &quot;&amp;&quot; oder dem Ende der Anfrage). Benutzerdefinierte Variablen können nicht auf die Befehle `layer=` und `effect=` angewendet werden. Im selben Befehlswert sind mehrere Variablen zulässig. Der Server ersetzt jedes Vorkommen von ` $ *`var`*$` durch *`value`*.

Variablenverweise dürfen nicht verschachtelt sein. Alle Vorkommen von ` $ *`var`*$` innerhalb von *`value`* werden nicht ersetzt.

Beispielsweise das Fragment Anfrage :

`$var2=apple&$var1=my$var2$tree&text=$var1$`

löst auf:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; ist kein reserviertes Zeichen; es kann auch anders in der Anfrage vorkommen. `src=my$image$file.tif` ist beispielsweise ein gültiger Befehl (vorausgesetzt, dass ein Katalogeintrag oder eine Bilddatei mit dem Namen `my$image$file.tif` vorhanden ist), `wid=$number$` ist es jedoch nicht, da `wid` ein numerisches Argument erfordert.

## Variablenverarbeitung in verschachtelten Anfragen {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$`-Verweise können überall in den geschweiften Klammern einer verschachtelten Bildbereitstellungs- oder Bildbereitstellungsanfrage auftreten, auch links neben &quot;?“ Trennen des Pfads von der Abfrage Der Server ersetzt diese Verweise durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anfrage weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle ` $ *`var`*=`-Definitionen aus der URL oder `catalog::Modifier` an alle verschachtelten Bildbereitstellungs- und Bildrendering-Anfragen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen für alle Vorlagen verfügbar sind, unabhängig von der Verschachtelungsebene.

Unabhängig von der Verschachtelungsebene muss bei Variablenwerten, die an einer beliebigen Stelle in verschachtelten Bild-Rendering- oder Bildbereitstellungsanfragen oder den zugehörigen `catalog::Modifier` ersetzt werden sollen, nur eine HTTP-Kodierung mit einem Durchgang angewendet werden.

## Variablenverarbeitung in eingebetteten Fremdanforderungen {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` Verweise, die überall in den geschweiften Klammern einer eingebetteten Fremdanforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt. Dadurch können eingebettete Fremdanfragen in einer Vorlage in einem Bildkatalog platziert werden.

Variablenwerte, die in fremde Anforderungen ersetzt werden sollen, müssen in der Regel doppelt kodiert werden, da keine erneute Kodierung erfolgt, bevor der Server versucht, die endgültige fremde URL zu übertragen.

## Variablenverarbeitung beim SVG von Dateien {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$`-Verweise können beim SVG von Dateien in Attributwerten und in `<text>` auftreten. Die Bildbereitstellung ersetzt diese durch die entsprechenden ` $ *`var`*=`-Definitionen, die auf der Anfrageverschachtelungsebene bekannt sind, auf der die SVG-Datei angegeben ist.

>[!NOTE]
>
>Jeder Variablenwert, der in einen `href` Attributwert ersetzt werden soll, muss doppelt URL-kodiert sein; alle anderen müssen einzeln kodiert sein.

## Vordefinierte Pfadvariable {#section-930d0dd12e8f49499becc9fe8df24092}

Der im Anfragepfad angegebene *`object`* wird der vordefinierten Variablen `*`$object zugewiesen`*`. &quot;` $ *`object`*$`&quot; kann an einer beliebigen Stelle in der Anfrage, in der von der Anfrage referenzierten Vorlage oder in einer verschachtelten/eingebetteten Anfrage platziert werden, wenn ein solches Objekt zulässig ist, einschließlich des Werts von `src=` und `mask=` und des Pfads einer verschachtelten/eingebetteten Anfrage.

Die folgende Anfrage verwendet beispielsweise das im Pfad angegebene Bild als Quelle einer Ebene in einer verschachtelten Anfrage:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Dies entspricht

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

Die Definition von `*`$object`*` kann überschrieben werden, indem explizit ` $ *`object`*=` mit dem gewünschten Wert angegeben wird.

Die vordefinierte Pfadvariable wird häufig in Verbindung mit `template=` verwendet.

## Standard {#section-b02483d15529444586a2e9504805b155}

Keine. Nur definierte Variablen werden durch den Server ersetzt (mit Ausnahme der vordefinierten Pfadvariablen $object, die immer ersetzt wird). Alle Vorkommen von ` $ *`var`*$` bleiben Literal, wenn `*`var`*` nicht mit einer vorhandenen Variablendefinition abgeglichen werden kann.

## Beispiele {#section-fba9393df6984247b7e30b3f93992e86}

Siehe Beispiel A in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
