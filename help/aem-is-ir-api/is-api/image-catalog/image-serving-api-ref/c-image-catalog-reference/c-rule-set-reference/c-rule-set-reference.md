---
description: Die Bildbereitstellung unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anfragen, der auf Regeln für Übereinstimmungen und Ersetzungen regulärer Ausdrücke basiert.
solution: Experience Manager
title: Referenz zum Regelsatz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Referenz zum Regelsatz{#rule-set-reference}

Die Bildbereitstellung unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anfragen, der auf Regeln für Übereinstimmungen und Ersetzungen regulärer Ausdrücke basiert.

Sammlungen von Vorverarbeitungsregeln (*Regelsätze)* Bildkatalogen oder dem Standardkatalog angehängt werden. Regeln im Standardkatalog gelten nur, wenn die Anfrage keinen bestimmten Hauptbildkatalog identifiziert.

Regeln für die Anfragevorverarbeitung können den Pfad und die Abfrageabschnitte von Anfragen ändern, bevor sie vom Parser des [!DNL Platform Server] verarbeitet werden, einschließlich der Bearbeitung des Pfads, des Hinzufügens von Befehlen, des Änderns von Befehlswerten und des Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Sicherheitsfunktionen zu konfigurieren und zu überschreiben, die normalerweise nur mit Katalogattributen gesteuert werden, z. B. Anfrageverschleierung, Wasserzeichen sowie die Beschränkung des Service auf bestimmte Client-IP-Adressen.

Regelsätze werden als XML-Dokumentdateien gespeichert. Der relative oder absolute Pfad der Regelsatzdatei muss in `attribute::RuleSetFile` angegeben werden.

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

Die `<?xml>`- und `<ruleset>`-Elemente sind immer in einer gültigen XML-Regelsatzdatei erforderlich, auch wenn keine tatsächlichen Regeln definiert sind.

Ein `<ruleset>`, das eine beliebige Anzahl `<rule>` Elemente enthält, ist zulässig.

Beim Inhalt der Vorverarbeitungsregeldateien wird zwischen Groß- und Kleinschreibung unterschieden.

## Validierung von Regelsätzen {#section-d8d101a0b4d74580835e37d128d05567}

Eine Kopie von [!DNL RuleSet.xsd] wird im Katalogordner bereitgestellt und sollte verwendet werden, um eine Regelsatzdatei zu validieren, bevor sie in der [!DNL catalog.ini]-Datei registriert wird. Beachten Sie, dass Image Serving eine interne Kopie von [!DNL RuleSet.xsd] zur Validierung verwendet.

## URL-Vorverarbeitung {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Vor jeder anderen Verarbeitung wird eine eingehende HTTP-Anfrage teilweise geparst, um zu bestimmen, welcher Bildkatalog angewendet werden soll. Sobald der Katalog identifiziert ist, wird der Regelsatz für den ausgewählten Katalog (oder der Standardkatalog, wenn kein bestimmter Katalog identifiziert wurde) angewendet.

Die `<rule>` werden in der Reihenfolge durchsucht, die für eine Übereinstimmung mit dem Inhalt des `<expression>` Elements angegeben ist ( *`expression`*).

Bei einer Übereinstimmung mit einer `<rule>` wird die optionale *`substitution`* angewendet und die geänderte Anforderungszeichenfolge zur normalen Verarbeitung an den Anforderungs-Parser des Servers übergeben.

Wenn beim Erreichen des `<ruleset>` keine erfolgreiche Übereinstimmung erzielt wird, wird die Anfrage ohne Änderung an den Parser übergeben.

## Das OnMatch-Attribut {#section-ed952fa55d99422db0ee68a2b9d395d3}

Das Standardverhalten kann mit dem Attribut `OnMatch` des `<rule>`-Elements geändert werden. `OnMatch` kann auf `break` (Standard), `continue` oder `error` festgelegt werden.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Element und Attribut</b> </th> 
   <th class="entry"> <b>Verhalten, wenn eine Übereinstimmung auftritt</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch=„break“&gt; </span> </p> </td> 
   <td> <p>Die Regelverarbeitung wird sofort beendet, nachdem die Ersetzung für diese Regel angewendet wurde. Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch=„continue“&gt; </span> </p> </td> 
   <td> <p>Die Ersetzung wird angewendet, und die Verarbeitung wird mit der nächsten Regel fortgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch=„error“&gt; </span> </p> </td> 
   <td> <p>Die Regelverarbeitung wird sofort beendet, und dem Client wird ein Antwortstatus „Anfrage abgelehnt“ zurückgegeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Katalogattribute überschreiben {#section-3f1e33a65c5346d1b4a69958c61432f3}

Das `rule`-Element kann optional Attribute definieren, die die entsprechenden Katalogattribute überschreiben, wenn die Regel erfolgreich abgeglichen wird. Wenn mehrere übereinstimmende Regeln dasselbe Attribut festlegen, hat die letzte Priorität. Unter [Regel](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md)-Element finden Sie eine Liste von Attributen, die mit Regeln gesteuert werden können.

## Reguläre Ausdrücke {#section-3f77bb9a265147b38c645f63ab1bad8b}

Eine einfache Zeichenfolgenabgleichung funktioniert für sehr einfache Anwendungen, aber in den meisten Fällen sind reguläre Ausdrücke erforderlich. Reguläre Ausdrücke sind zwar dem Industriestandard entsprechend, die spezifische Implementierung variiert jedoch von Instanz zu Instanz.

[[!DNL package java.util.regex]](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschreibt die spezifische Implementierung regulärer Ausdrücke, die von Image-Serving verwendet wird.

## Erfasste Teilzeichenfolgen {#section-066e659406d5403599cd26ae35e80d68}

Um komplexe URL-Änderungen zu erleichtern, können Unterzeichenfolgen im Ausdruck erfasst werden, indem die Unterzeichenfolge in Klammern (…) eingeschlossen wird. Erfasste Teilzeichenfolgen werden entsprechend der Position der führenden Klammer sequenziell mit 1 beginnend nummeriert. Die erfassten Teilzeichenfolgen können in die Ersetzung eingefügt werden, indem ` $ *`n`*` verwendet wird, wobei *`n`* die Sequenznummer der erfassten Teilzeichenfolge ist.

## Verwalten von Regelsatzdateien {#section-0598a608e4044bb4805fe93ceebe10a9}

Jedem Bildkatalog kann mit dem Katalogattribut `attribute::RuleSetFile` eine Regelsatzdatei angehängt werden. Sie können die Regelsatzdatei zwar jederzeit bearbeiten, der Bildserver erkennt die Änderungen jedoch nur, wenn der zugehörige Bildkatalog neu geladen wird. Dieses Neuladen erfolgt, wenn der Platform-Server gestartet oder neu gestartet wird und wenn die primäre Katalogdatei, die das Dateisuffix &quot;[!DNL .ini]&quot; aufweist, geändert oder „berührt“ wird, um das Dateidatum zu ändern.

## Beispiele {#section-aa769437d967459299b83a4bf34fe924}

**Beispiel A.** Definieren Sie eine Regel, die die Bildqualitätseinstellungen erhöht, wenn der Bildname das Suffix &quot;[!DNL _hg]&quot; aufweist:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

Der Regelausdruck gibt eine Übereinstimmung (ohne Berücksichtigung der Groß-/Kleinschreibung) von &quot;[!DNL _hg]&quot; am Ende der URL-Zeichenfolge an. Das Suffix wird durch die angegebene Abfragezeichenfolge ersetzt, wodurch die Bildqualitätseinstellungen geändert werden. Beachten Sie, dass das `?` in der Ersatzzeichenfolge maskiert ist, da dies ein Sonderzeichen in regulären Ausdrücken ist.

>[!NOTE]
>
>Die erforderliche Kodierung für das kaufmännische Und-Zeichen. Alternativ kann die Ersatzzeichenfolge in einen CDATA-Block eingeschlossen werden:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Beispiel B** Eine bestimmte Web-Anwendung lässt keine Abfragezeichenfolgen zu. Definieren Sie eine Regel, die das nachgestellte Pfadelement `small`, `medium` oder `large` in eine Vorlage übersetzt, wobei der Rest des Pfads als Bildname verwendet wird. `myCat/myImage/small` würde beispielsweise in `myCat/smallTemplate?src=myCat/myImage` übersetzt werden.

Wir können Teilzeichenfolgen verwenden, um die Anfrage neu zu strukturieren:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Verwandte Themen {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
