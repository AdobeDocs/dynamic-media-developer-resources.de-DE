---
description: Ersatzvariablen werden verwendet, um Werte von der Anforderungs-URL an in Bildkatalogen gespeicherte Komponentenvorlagen zu übertragen. Variablen können auch verwendet werden, um denselben Wert an verschiedene Stellen in einer komplexen Anforderung zu vermitteln.
solution: Experience Manager
title: Ersatzvariablen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
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
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Wert, auf den die Variable gesetzt werden soll (Zeichenfolge). </p> </td> 
 </tr> 
</table>

Variablendefinitionen und -verweise können im Abfrageabschnitt der Anforderung auftreten, in `catalog::Modifier`und in `catalog::PostModifier`.

Variablen werden wie oben definiert, ähnlich wie andere IS-Befehle; Der vorangestellte &#39;$&#39; gibt den Befehl als Variablendefinition an. Variablen müssen definiert werden, bevor sie referenziert werden.

Der Variablenname *`var`* nicht zwischen Groß- und Kleinschreibung unterscheiden und aus einer beliebigen Kombination aus ASCII-Buchstaben, Zahlen, &#39;-&#39;, &#39;_&#39; und &#39;.&#39; bestehen können.

>[!NOTE]
>
>*`value`* muss URL-kodiert mit einem Durchgang sein, um eine sichere HTTP-Übertragung zu ermöglichen. Eine Doppelkodierung ist erforderlich, wenn *`value`* wird über HTTP erneut übertragen. Dies ist der Fall, wenn *`value`* wird in eine verschachtelte ausländische Anforderung oder in das href-Attribut einer SVG ersetzt `<image>` -Element.

Variablenverweise bestehen aus dem Variablennamen, der durch das vorangestellte und nachfolgende &#39;$&#39; ($) getrennt wird *var*$). Verweise können an einer beliebigen Stelle im Werteteil beliebiger IS-Befehle auftreten (d. h. zwischen dem &#39;=&#39; nach dem Befehlsnamen und dem nachfolgenden &#39;&amp;&#39; oder dem Ende der Anfrage). Benutzerdefinierte Variablen können nicht auf die `layer=` und `effect=` Befehle. Im selben Befehlswert sind mehrere Variablen zulässig. Der Server ersetzt jedes Vorkommen von ` $ *`var`*$` mit *`value`*.

Variablenverweise sind möglicherweise nicht verschachtelt. Alle Vorkommnisse von ` $ *`var`*$` Innerhalb *`value`* nicht ersetzt werden.

Beispielsweise das Anforderungsfragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

löst Folgendes auf:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; ist kein reserviertes Zeichen; kann es andernfalls in der Anfrage auftreten. Beispiel: `src=my$image$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Katalogeintrag oder eine Bilddatei mit dem Namen `my$image$file.tif` ist vorhanden), während `wid=$number$` nicht, weil `wid` erfordert ein numerisches Argument.

## Variablenverarbeitung in verschachtelten Anforderungen {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` -Verweise können an einer beliebigen Stelle in den geschweiften Klammern einer verschachtelten Image Serving- oder Image Rendering-Anforderung auftreten, auch links neben &quot;?&quot; Trennen Sie den Pfad von der Abfrage. Der Server ersetzt diese Verweise durch Werte (entweder aus der URL oder aus `catalog::Modifier` des Hauptbildkatalogs) vor der weiteren Analyse und Verarbeitung der verschachtelten Anforderung.

Darüber hinaus werden alle ` $ *`var`*=` Definitionen aus der URL oder `catalog::Modifier` werden an alle verschachtelten Image Serving- und Image Rendering-Anforderungen weitergeleitet. Dadurch wird sichergestellt, dass alle Variablendefinitionen unabhängig von der Verschachtelungsebene für alle Vorlagen verfügbar sind.

Unabhängig von der Verschachtelungsstufe darf nur die HTTP-Kodierung mit einem Durchgang auf Variablenwerte angewendet werden, die an einer beliebigen Stelle in verschachtelten Image Rendering- oder Image Serving-Anforderungen oder den zugehörigen zugehörigen Anforderungen ersetzt werden sollen `catalog::Modifier` Zeichenfolgen.

## Variablenverarbeitung in eingebetteten ausländischen Anforderungen {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` Verweise, die an einer beliebigen Stelle in den geschweiften Klammern einer eingebetteten ausländischen Anforderung auftreten, werden durch übereinstimmende Variablendefinitionswerte ersetzt. Dadurch können eingebettete ausländische Anforderungen in eine Vorlage in einem Bildkatalog eingefügt werden.

Variablenwerte, die in ausländische Anforderungen ersetzt werden sollen, müssen in der Regel doppelt kodiert sein, da keine Neukodierung angewendet wird, bevor der Server versucht, die endgültige ausländische URL zu übertragen.

## Variablenverarbeitung in SVG-Dateien {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` -Verweise können in SVG-Dateien in Attributwerten und in `<text>` Zeichenfolgen. Image Serving ersetzt diese mit dem entsprechenden ` $ *`var`*=` Definitionen, die auf der Anfrageverschachtelungsebene bekannt sind, auf der die SVG-Datei angegeben ist.

>[!NOTE]
>
>Jeder Variablenwert, der durch einen `href` -Attributwert muss doppelt URL-kodiert sein; alle anderen müssen einzeln kodiert sein.

## Vordefinierte Pfadvariable {#section-930d0dd12e8f49499becc9fe8df24092}

Die *`object`* wird im Anfragepfad angegeben und der vordefinierten Variablen zugewiesen `*`$object`*`. &#39; ` $ *`Objekt`*$`&quot; kann an einer beliebigen Stelle in der Anfrage, in der von der Anfrage referenzierten Vorlage oder in einer verschachtelten/eingebetteten Anforderung platziert werden, in der ein solches Objekt zulässig ist, einschließlich des Werts von `src=` und `mask=`und den Pfad einer verschachtelten/eingebetteten Anforderung.

Beispielsweise wird mit der folgenden Anfrage das im Pfad angegebene Bild als Quelle einer Ebene in einer verschachtelten Anforderung wiederverwendet:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Dies entspricht

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

Die Definition von `*`$object`*` kann überschrieben werden, indem Sie explizit ` $ *`Objekt`*=` mit dem gewünschten Wert.

Die vordefinierte Pfadvariable wird häufig zusammen mit `template=`.

## Standard {#section-b02483d15529444586a2e9504805b155}

Keine. Nur definierte Variablen werden vom Server ersetzt (mit Ausnahme der vordefinierten Pfadvariablen $object, die immer ersetzt wird). Alle Vorkommnisse von ` $ *`var`*$` bleiben literal, wenn `*`var`*`kann nicht mit einer vorhandenen Variablendefinition übereinstimmen.

## Beispiele {#section-fba9393df6984247b7e30b3f93992e86}

Siehe &quot;Beispiel A&quot;in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
