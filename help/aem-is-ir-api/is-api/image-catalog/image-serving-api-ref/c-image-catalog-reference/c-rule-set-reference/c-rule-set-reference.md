---
description: Image Serving unterstützt einen einfachen Anfragevorverarbeitungsmechanismus, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.
solution: Experience Manager
title: Regelsatzreferenz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Regelsatzreferenz{#rule-set-reference}

Image Serving unterstützt einen einfachen Anfragevorverarbeitungsmechanismus, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.

Kollektionen von Vorab-Verarbeitungsregeln (*Regelsätze*) können an Bildkataloge oder den Standardkatalog angehängt werden. Regeln im Standardkatalog gelten nur, wenn die Anforderung keinen bestimmten Hauptbildkatalog identifiziert.

Die Vorab-Verarbeitungsregeln für Anfragen können den Pfad und die Anfrageabschnitte ändern, bevor sie vom Parser des Platform-Servers verarbeitet werden. Dazu gehören das Manipulieren des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Sicherheitsfunktionen zu konfigurieren und zu überschreiben, die normalerweise nur mit Katalogattributen gesteuert werden, z. B. Anforderungsverschleierung, Wasserzeichen und Beschränkung des Diensts auf bestimmte Client-IP-Adressen.

Regelsätze werden als XML-Dokumentdateien gespeichert. Der relative oder absolute Pfad der Regelsatzdatei muss in `attribute::RuleSetFile`.

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

Die `<?xml>` und `<ruleset>` -Elemente sind immer in einer gültigen XML-Regelsatz-Datei erforderlich, auch wenn keine tatsächlichen Regeln definiert sind.

One `<ruleset>` Element mit beliebiger Anzahl von `<rule>` -Elemente erlaubt sind.

Beim Inhalt von Regeldateien zur Vorverarbeitung wird zwischen Groß- und Kleinschreibung unterschieden.

## Regelsatzvalidierung {#section-d8d101a0b4d74580835e37d128d05567}

Eine Kopie von [!DNL RuleSet.xsd] wird im Katalogordner bereitgestellt und sollte verwendet werden, um eine Regelsatzdatei vor der Registrierung in der [!DNL catalog.ini] -Datei. Beachten Sie, dass Image Serving eine interne Kopie von [!DNL RuleSet.xsd] zur Validierung.

## URL-Vorverarbeitung {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Vor jeder anderen Verarbeitung wird eine eingehende HTTP-Anforderung teilweise analysiert, um zu bestimmen, welcher Bildkatalog angewendet werden soll. Sobald der Katalog identifiziert wurde, wird der Regelsatz für den ausgewählten Katalog (oder der Standardkatalog, wenn kein bestimmter Katalog identifiziert wurde) angewendet.

Die `<rule>` -Elemente in der Reihenfolge durchsucht werden, die für eine Übereinstimmung mit dem Inhalt der `<expression>` Element ( *`expression`*).

Wenn eine `<rule>` zugeordnet wird, wird das optionale *`substitution`* wird angewendet und die geänderte Anforderungszeichenfolge wird zur normalen Verarbeitung an den Anforderungsparser des Servers übergeben.

Wenn keine erfolgreiche Übereinstimmung beim Ende des `<ruleset>` erreicht wird, wird die Anforderung ohne Änderung an den Parser übergeben.

## Das OnMatch-Attribut {#section-ed952fa55d99422db0ee68a2b9d395d3}

Das Standardverhalten kann mit dem `OnMatch` -Attribut `<rule>` -Element. `OnMatch` kann auf `break` (Standard), `continue`oder `error`.

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
   <td> <p>Die Regelverarbeitung wird sofort beendet, nachdem die Ersetzung für diese Regel vorgenommen wurde. Standard. </p> </td> 
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

## Überschreiben von Katalogattributen {#section-3f1e33a65c5346d1b4a69958c61432f3}

Die `rule` -Element kann optional Attribute definieren, die die entsprechenden Katalogattribute überschreiben, wenn die Regel erfolgreich abgeglichen wird. Wenn mehrere übereinstimmende Regeln dasselbe Attribut festlegen, hat das letzte Vorrang. Siehe [Regel](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) -Element für eine Liste von Attributen, die mit Regeln gesteuert werden können.

## Reguläre Ausdrücke {#section-3f77bb9a265147b38c645f63ab1bad8b}

Einfache Zeichenfolgenabgleiche funktionieren für sehr einfache Anwendungen, aber in den meisten Fällen sind reguläre Ausdrücke erforderlich. Während reguläre Ausdrücke den Branchenstandard aufweisen, variiert die spezifische Implementierung von Instanz zu Instanz.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschreibt die spezifische Implementierung regulärer Ausdrücke, die von Image Serving verwendet wird.

## Erfasste Unterzeichenfolgen {#section-066e659406d5403599cd26ae35e80d68}

Um komplexe URL-Änderungen zu erleichtern, können Unterzeichenfolgen im Ausdruck erfasst werden, indem die Unterzeichenfolge in Klammern (...) eingeschlossen wird. Erfasste Teilzeichenfolgen werden in der Reihenfolge mit 1 beginnend gemäß der Position der führenden Klammer nummeriert. Die erfassten Teilzeichenfolgen können in die Substitution mit ` $ *`n`*`, wobei *`n`* ist die Sequenznummer der erfassten Teilzeichenfolge.

## Verwalten von Regelsatzdateien {#section-0598a608e4044bb4805fe93ceebe10a9}

An jeden Bildkatalog mit dem Katalogattribut kann eine Regelsatzdatei angehängt werden `attribute::RuleSetFile`. Sie können die Regelsatzdatei zwar jederzeit bearbeiten, der Bildserver erkennt die Änderungen jedoch nur, wenn der zugehörige Bildkatalog neu geladen wird. Diese Neuladung erfolgt, wenn der Plattformserver gestartet oder neu gestartet wird und wenn die primäre Katalogdatei über eine [!DNL .ini] -Dateisuffix, geändert oder &quot;geändert&quot;wird, um das Dateidatum zu ändern.

## Beispiele {#section-aa769437d967459299b83a4bf34fe924}

**Beispiel A.** Definieren Sie eine Regel, die die Bildqualitätseinstellungen erhöht, wenn der Bildname das Suffix &quot; [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

Der Regelausdruck gibt einen Treffer an, bei dem nicht zwischen Groß- und Kleinschreibung unterschieden wird: [!DNL _hg]&quot; am Ende der URL-Zeichenfolge. Das Suffix wird durch die angegebene Abfragezeichenfolge ersetzt, die die Bildqualitätseinstellungen ändert. Beachten Sie Folgendes: `?` -Zeichen in der Ersatzzeichenfolge ist maskiert, da es sich um ein Sonderzeichen in regulären Ausdrücken handelt.

>[!NOTE]
>
>Die erforderliche Kodierung für das kaufmännische Und-Zeichen. Alternativ kann die Ersatzzeichenfolge in einen CDATA-Block eingeschlossen werden:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Beispiel B.** Eine bestimmte Webanwendung lässt keine Abfragezeichenfolgen zu. Definieren einer Regel, die das nachfolgende Pfadelement übersetzt `small`, `medium`oder `large` zu einer Vorlage hinzufügen, wobei der restliche Pfad als Bildname verwendet wird. Beispiel: `myCat/myImage/small` würde übersetzen in `myCat/smallTemplate?src=myCat/myImage`.

Wir können Unterzeichenfolgen verwenden, um die Anforderung neu zu strukturieren:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Verwandte Themen {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
