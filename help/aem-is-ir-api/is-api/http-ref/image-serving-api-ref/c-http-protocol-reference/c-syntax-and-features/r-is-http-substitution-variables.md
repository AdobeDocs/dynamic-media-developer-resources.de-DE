---
description: Ersatzvariablen werden verwendet, um Werte von der Anforderungs-URL an in Bildkatalogen gespeicherte Komponentenvorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anforderung zu vermitteln.
solution: Experience Manager
title: Ersatzvariablen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Ersatzvariablen{#substitution-variables}

Ersatzvariablen werden verwendet, um Werte von der Anforderungs-URL an in Bildkatalogen gespeicherte Komponentenvorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anforderung zu vermitteln.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variablenname. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable gesetzt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

Variablendefinitionen und -verweise können im Abfrageabschnitt der Anforderung, in `catalog::Modifier` und in `catalog::PostModifier` auftreten.

Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle; der vorangestellte &#39;$&#39; identifiziert den Befehl als Variablendefinition. Variablen müssen definiert werden, bevor sie referenziert werden.

Beim Variablennamen &quot;*`var`*&quot; wird nicht zwischen Groß- und Kleinschreibung unterschieden und es kann sich um eine beliebige Kombination aus ASCII-Buchstaben, Zahlen, &#39;-&#39;, &#39;_&#39; und &#39;.&#39; handeln.

>[!NOTE]
>
>*`value`* muss URL-kodiert mit Einzeldurchlauf sein, um eine sichere HTTP-Übertragung zu ermöglichen. Eine Doppelkodierung ist erforderlich, wenn *`value`* über HTTP erneut übertragen wird. Dies ist der Fall, wenn *`value`* durch eine verschachtelte ausländische Anforderung oder durch das href-Attribut eines SVG `<image>` -Elements ersetzt wird.

Variablenverweise bestehen aus dem Variablennamen, der durch das Voranstellen und Nachstellen von &#39;$&#39; ($*var*$) getrennt wird. Verweise können an einer beliebigen Stelle im Werteteil beliebiger IS-Befehle auftreten (d. h. zwischen dem &#39;=&#39; nach dem Befehlsnamen und dem nachfolgenden &#39;&amp;&#39; oder dem Ende der Anfrage). Benutzerdefinierte Variablen können nicht auf die Befehle `layer=` und `effect=` angewendet werden. Im selben Befehlswert sind mehrere Variablen zulässig. Der Server ersetzt jedes Vorkommen von ` $ *`var`*$` durch *`value`*.

Variablenverweise sind möglicherweise nicht verschachtelt. Alle Vorkommnisse von ` $ *`var`*$` innerhalb von *`value`* werden nicht ersetzt.

Beispielsweise das Anforderungsfragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

löst Folgendes auf:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; ist kein reserviertes Zeichen; es kann andernfalls in der Anfrage auftreten. Beispiel: `src=my$image$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Katalogeintrag oder eine Bilddatei mit dem Namen `my$image$file.tif` vorhanden ist), während `wid=$number$` nicht ist, da `wid` ein numerisches Argument erfordert.

## Variablenverarbeitung in verschachtelten Anforderungen {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` -Verweise können an einer beliebigen Stelle in den geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben &quot;?&quot; Trennen Sie den Pfad von der Abfrage. Der Server ersetzt diese Verweise durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs), bevor die verschachtelte Anforderung weiter analysiert und verarbeitet wird.

Darüber hinaus werden alle ` $ *`var`*=` -Definitionen aus der URL oder `catalog::Modifier` an alle verschachtelten Image Serving- und Image Rendering-Anforderungen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen unabhängig von der Verschachtelungsebene für alle Vorlagen verfügbar sind.

Unabhängig von der Verschachtelungsstufe darf nur eine einmalige HTTP-Kodierung auf Variablenwerte angewendet werden, die an einer beliebigen Stelle in verschachtelten Image Rendering- oder Image Serving-Anforderungen oder den zugehörigen `catalog::Modifier` -Zeichenfolgen ersetzt werden sollen.

## Variablenverarbeitung in eingebetteten ausländischen Anforderungen {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` Verweise, die an einer beliebigen Stelle in den geschweiften Klammern einer eingebetteten ausländischen Anforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt. Dadurch können eingebettete ausländische Anforderungen in eine Vorlage in einem Bildkatalog eingefügt werden.

Variablenwerte, die in ausländische Anforderungen ersetzt werden sollen, müssen in der Regel doppelt kodiert sein, da keine Neukodierung angewendet wird, bevor der Server versucht, die endgültige ausländische URL zu übertragen.

## Variablenverarbeitung in SVG-Dateien {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` -Verweise können in SVG-Dateien in Attributwerten und in `<text>` -Zeichenfolgen auftreten. Image Serving ersetzt diese mit den entsprechenden ` $ *`var`*=` -Definitionen, die auf der Anfragenverschachtelungsebene bekannt sind, auf der die SVG-Datei angegeben ist.

>[!NOTE]
>
>Jeder Variablenwert, der in einen &quot;`href`&quot;-Attributwert ersetzt werden soll, muss doppelt URL-kodiert sein. Alle anderen müssen einzeln kodiert werden.

## Vordefinierte Pfadvariable {#section-930d0dd12e8f49499becc9fe8df24092}

Die im Anfragepfad angegebene *`object`* wird der vordefinierten Variablen `*`$object`*` zugewiesen. &quot;` $ *`object`*$`&quot; kann an einer beliebigen Stelle in der Anforderung, in der von der Anforderung referenzierten Vorlage oder in einer verschachtelten/eingebetteten Anforderung platziert werden, in der ein solches Objekt zulässig ist, einschließlich des Werts `src=` und `mask=` und des Pfads einer verschachtelten/eingebetteten Anforderung.

Beispielsweise verwendet die folgende Anfrage das im Pfad angegebene Bild als Quelle einer Ebene in einer verschachtelten Anforderung erneut:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Dies entspricht

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

Die Definition von `*`$object`*` kann überschrieben werden, indem explizit ` $ *`object`*=` mit dem gewünschten Wert angegeben wird.

Die vordefinierte Pfadvariable wird häufig zusammen mit `template=` verwendet.

## Standard {#section-b02483d15529444586a2e9504805b155}

Keine. Nur definierte Variablen werden vom Server ersetzt (mit Ausnahme der vordefinierten Pfadvariablen $object, die immer ersetzt wird). Alle Vorkommnisse von ` $ *`var`*$` bleiben literal, wenn `*`var`*` nicht mit einer vorhandenen Variablendefinition abgeglichen werden kann.

## Beispiele {#section-fba9393df6984247b7e30b3f93992e86}

Siehe &quot;Beispiel A&quot;in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
