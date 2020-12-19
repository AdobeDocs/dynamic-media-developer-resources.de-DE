---
description: Image Serving unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anforderungen, der auf Regeln für die Übereinstimmung und Ersetzung von regulären Ausdrücken basiert.
seo-description: Image Serving unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anforderungen, der auf Regeln für die Übereinstimmung und Ersetzung von regulären Ausdrücken basiert.
seo-title: Regelsatz
solution: Experience Manager
title: Regelsatz
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 0%

---


# Regelsatzverweis{#rule-set-reference}

Image Serving unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anforderungen, der auf Regeln für die Übereinstimmung und Ersetzung von regulären Ausdrücken basiert.

Sammlungen von Vorverarbeitungsregeln (*Regelsätze*) können an Bildkataloge oder den Standardkatalog angehängt werden. Regeln im Standardkatalog gelten nur, wenn die Anforderung keinen bestimmten Hauptbildkatalog identifiziert.

Vorverarbeitungsregeln für Anfragen können den Pfad und die Abfrage von Anforderungen ändern, bevor sie vom Parser des Plattformservers verarbeitet werden. Dazu gehören die Änderung des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Sicherheitsfunktionen zu konfigurieren und außer Kraft zu setzen, die normalerweise nur mit Katalogattributen gesteuert werden, wie z. B. Anforderungsvertuschung, Wasserkennzeichnung und Beschränkung des Diensts auf bestimmte IP-Adressen von Clients.

Regelsätze werden als XML-Dokument-Dateien gespeichert. Der relative oder absolute Pfad der Regelsatzdatei muss in `attribute::RuleSetFile` angegeben werden.

## Allgemeine Struktur {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

Die Elemente `<?xml>` und `<ruleset>` sind immer in einer gültigen XML-Regelsatzdatei erforderlich, auch wenn keine tatsächlichen Regeln definiert sind.

Ein `<ruleset>`-Element, das eine beliebige Anzahl von `<rule>`-Elementen enthält, ist zulässig.

Beim Inhalt der Regeldateien zur Vorverarbeitung wird die Groß-/Kleinschreibung beachtet.

## Regelsatzüberprüfung {#section-d8d101a0b4d74580835e37d128d05567}

Eine Kopie von [!DNL RuleSet.xsd] wird im Katalogordner bereitgestellt und sollte zur Überprüfung einer Regelsatzdatei verwendet werden, bevor sie in der Datei [!DNL catalog.ini] registriert wird. Beachten Sie, dass Image Serving eine interne Kopie von [!DNL RuleSet.xsd] zur Überprüfung verwendet.

## URL-Vorverarbeitung {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Vor jeder anderen Verarbeitung wird eine eingehende HTTP-Anforderung teilweise analysiert, um zu bestimmen, welcher Bildkatalog angewendet werden soll. Sobald der Katalog identifiziert wurde, wird der Regelsatz für den ausgewählten Katalog (oder der Standardkatalog, wenn kein bestimmter Katalog identifiziert wurde) angewendet.

Die `<rule>`-Elemente werden in der angegebenen Reihenfolge nach dem Inhalt des `<expression>`-Elements ( *`expression`*) gesucht.

Wenn eine `<rule>`-Übereinstimmung vorliegt, wird die optionale *`substitution`*-Zeichenfolge angewendet und die geänderte Anforderungs-Zeichenfolge wird zur normalen Verarbeitung an den Anforderungsparser des Servers übergeben.

Wenn beim Erreichen des Endes von `<ruleset>` keine erfolgreiche Übereinstimmung erfolgt, wird die Anforderung ohne Änderung an den Parser übergeben.

## Das OnMatch-Attribut {#section-ed952fa55d99422db0ee68a2b9d395d3}

Das Standardverhalten kann mit dem `OnMatch`-Attribut des `<rule>`-Elements geändert werden. `OnMatch` kann auf  `break` (Standard),  `continue`oder  `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Element und Attribut</b> </th> 
   <th class="entry"> <b>Verhalten bei Übereinstimmung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>Die Regelverarbeitung wird unmittelbar nach der Anwendung der Ersetzung für diese Regel beendet. Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>Die Ersetzung wird angewendet und die Verarbeitung wird mit der nächsten Regel fortgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>Die Regelverarbeitung wird sofort beendet und der Antwortstatus "Anfrage verweigert"wird an den Client zurückgegeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Außerkraftsetzen von Katalogattributen {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` -Elemente können optional Attribute definieren, die die entsprechenden Katalogattribute überschreiben, wenn die Regel erfolgreich übereinstimmt. Wenn mehrere übereinstimmende Regeln dasselbe Attribut festlegen, wird das letzte Attribut beibehalten. Eine Liste der Attribute, die mit Regeln gesteuert werden können, finden Sie in der Beschreibung des Elements ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`.

## Reguläre Ausdruck {#section-3f77bb9a265147b38c645f63ab1bad8b}

Einfache Zeichenfolgenübereinstimmung funktioniert bei sehr einfachen Anwendungen, in den meisten Fällen sind jedoch reguläre Ausdruck erforderlich. Während reguläre Ausdruck Branchenstandard sind, variiert die spezifische Implementierung von Instanz zu Instanz.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschreibt die spezielle Implementierung des regulären Ausdrucks, die von Image Serving verwendet wird.

## Erfasste Teilzeichenfolgen {#section-066e659406d5403599cd26ae35e80d68}

Um komplexe URL-Änderungen zu erleichtern, können Teilzeichenfolgen im Ausdruck erfasst werden, indem sie die Unterzeichenfolge mit Klammern (...) versehen. Erfasste Teilzeichenfolgen werden entsprechend der Position der führenden Klammer sequenziell mit 1 nummeriert. Die erfassten Unterzeichenfolgen können mit ` $ *`n`*` in die Ersetzung eingefügt werden, wobei *`n`* die Sequenznummer der erfassten Unterzeichenfolge ist.

## Verwalten von Regelsatzdateien {#section-0598a608e4044bb4805fe93ceebe10a9}

Eine Regelsatzdatei kann mit dem Katalogattribut `attribute::RuleSetFile` an jeden Bildkatalog angehängt werden. Während Sie die Regelsatzdatei jederzeit bearbeiten können, erkennt der Image-Server die Änderungen nur, wenn der zugehörige Bildkatalog neu geladen wird. Dieses Neuladen erfolgt, wenn der Plattformserver gestartet oder neu gestartet wird und die primäre Katalogdatei, die das Suffix [!DNL .ini] enthält, geändert oder &quot;angefasst&quot;wird, um das Dateidatum zu ändern.

## Beispiele {#section-aa769437d967459299b83a4bf34fe924}

**Beispiel A.** Definieren Sie eine Regel, die die Bildqualitätseinstellungen erhöht, wenn der Bildname das Suffix &quot;  [!DNL _hg]&quot; hat:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

Der Ausdruck rule gibt eine Groß-/Kleinschreibung ohne Unterscheidung von &quot; [!DNL _hg]&quot;am Ende der URL-Zeichenfolge an. Das Suffix wird durch die angegebene Abfrage ersetzt, die die Bildqualitätseinstellungen ändert. Beachten Sie, dass das Zeichen `?` in der Ersatzzeichenfolge mit Escape-Zeichen versehen ist, da es sich um ein Sonderzeichen in regulären Ausdrücken handelt.

>[!NOTE]
>
>Die erforderliche Kodierung für das kaufmännische Zeichen. Alternativ könnte die Ersatzzeichenfolge in einen CDATA-Block eingeschlossen werden:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Beispiel B.** Eine bestimmte Webanwendung lässt keine Zeichenfolgen für die Abfrage zu. Definieren Sie eine Regel, die das nachfolgende Pfadelement `small`, `medium` oder `large` in eine Vorlage übersetzt, wobei der Rest des Pfads als Bildname verwendet wird. Beispiel: `myCat/myImage/small` würde in `myCat/smallTemplate?src=myCat/myImage` übersetzen.

Wir können Unterzeichenfolgen verwenden, um die Anforderung umzustrukturieren:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Verwandte Themen {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
