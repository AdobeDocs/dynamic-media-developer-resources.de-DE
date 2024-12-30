---
description: Das Bild-Rendering unterstützt einen einfachen Vorverarbeitungsmechanismus für Anfragen, der auf Regeln für Übereinstimmungen und Ersetzungen regulärer Ausdrücke basiert.
solution: Experience Manager
title: Referenz zum Regelsatz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Referenz zum Regelsatz{#rule-set-reference}

Das Bild-Rendering unterstützt einen einfachen Vorverarbeitungsmechanismus für Anfragen, der auf Regeln für Übereinstimmungen und Ersetzungen regulärer Ausdrücke basiert.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Sammlungen von Vorverarbeitungsregeln (*Regelsätze*) können entweder an Materialkataloge oder an den Standardkatalog angehängt werden. Regeln im Standardkatalog gelten nur, wenn die Anfrage keinen bestimmten Materialkatalog anhängt.

Regeln für die Anfragevorverarbeitung können den Pfad und die Abfrageanteile von Anfragen ändern, bevor sie vom Anfrage-Parser des Servers verarbeitet werden, einschließlich der Bearbeitung des Pfads, des Hinzufügens von Befehlen, des Änderns von Befehlswerten und des Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um einige Katalogattribute zu konfigurieren und zu überschreiben sowie den Service auf bestimmte Client-IP-Adressen zu beschränken.

Regelsätze werden als XML-Dokumentdateien gespeichert. Der relative oder absolute Pfad der Regelsatzdatei muss in `attribute::RuleSetFile` angegeben werden.

## Allgemeine Struktur {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

Die `<?xml>`-, `<!DOCTYPE>`- und `<ruleset>`-Elemente sind immer in einer gültigen XML-Regelsatzdatei erforderlich, auch wenn keine tatsächlichen Regeln definiert sind.

Ein `<ruleset>`, das eine beliebige Anzahl `<rule>` Elemente enthält, ist zulässig.

Beim Inhalt der Vorverarbeitungsregeldateien wird zwischen Groß- und Kleinschreibung unterschieden.

## URL-Vorverarbeitung {#section-737a38d1b8c746f995e64fa6cfbcec87}

Vor jeder anderen Verarbeitung wird eine eingehende HTTP-Anfrage teilweise geparst, um zu bestimmen, welcher Materialkatalog angewendet werden soll. Sobald der Katalog identifiziert ist, wird der Regelsatz für den ausgewählten Katalog (oder der Standardkatalog, wenn kein bestimmter Katalog identifiziert wurde) angewendet.

Die `<rule>` werden in der Reihenfolge durchsucht, die für eine Übereinstimmung mit dem Inhalt des `<expression>` Elements angegeben ist ( *`expression`*).

Bei einer Übereinstimmung mit einer `<rule>` wird die optionale *`substitution`* angewendet und die geänderte Anforderungszeichenfolge zur normalen Verarbeitung an den Anforderungs-Parser des Servers übergeben.

Wenn beim Erreichen des `<ruleset>` keine erfolgreiche Übereinstimmung erzielt wird, wird die Anfrage ohne Änderung an den Parser übergeben.

## Das OnMatch-Attribut {#section-7a8ad3597780486985af5e9a3b1c7b56}

Das Standardverhalten kann mit dem Attribut `OnMatch` der `<rule>` Elemente geändert werden. `OnMatch` kann auf `break` (Standard), `continue` oder `error.` festgelegt werden

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element und Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Verhalten, wenn eine Übereinstimmung auftritt </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch=„break“&gt;</span> </p> </td> 
   <td colname="col2"> <p>Die Regelverarbeitung wird sofort beendet, nachdem die Ersetzung für diese Regel angewendet wurde. Standard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch=„continue“&gt;</span> </p> </td> 
   <td colname="col2"> <p>Die Ersetzung wird angewendet, und die Verarbeitung wird mit der nächsten Regel fortgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch=„error“&gt;</span> </p> </td> 
   <td colname="col2"> <p>Die Regelverarbeitung wird sofort beendet, und dem Client wird ein Antwortstatus „Anfrage abgelehnt“ zurückgegeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Katalogattribute überschreiben {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` können optional Attribute definieren, die die entsprechenden Katalogattribute überschreiben, wenn die Regel erfolgreich abgeglichen und `OnMatch="break"` festgelegt wurde. Wenn `OnMatch="continue"` festgelegt ist, werden keine Attribute angewendet. Unter der Beschreibung von `<rule>` finden Sie eine Liste von Attributen, die mit Regeln gesteuert werden können.

## Reguläre Ausdrücke {#section-4d326507b52544b0960a9a5f303e3fe6}

Eine einfache Zeichenfolgenabgleichung funktioniert für sehr einfache Anwendungen, aber in den meisten Fällen sind reguläre Ausdrücke erforderlich. Reguläre Ausdrücke sind zwar dem Industriestandard entsprechend, die spezifische Implementierung variiert jedoch von Instanz zu Instanz.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschreibt die spezifische Implementierung regulärer Ausdrücke, die von Image Serving verwendet wird.

## Erfasste Teilzeichenfolgen {#section-8057cd65d48949ffb6a50e929bd3688b}

Um komplexe URL-Änderungen zu erleichtern, können Unterzeichenfolgen im Ausdruck erfasst werden, indem die Unterzeichenfolge in Klammern (…) eingeschlossen wird. Erfasste Teilzeichenfolgen werden entsprechend der Position der führenden Klammer sequenziell mit 1 beginnend nummeriert. Die erfassten Teilzeichenfolgen können mithilfe von *`$n`* in die Ersetzung eingefügt werden, wobei *`n`* die Sequenznummer der erfassten Teilzeichenfolge ist.

## Verwalten von Regelsatzdateien {#section-e8ce976b56404c009496426fd334d23d}

Jedem Materialkatalog kann mit dem Katalogattribut `attribute::RuleSetFile` eine Regelsatzdatei angehängt werden. Sie können die Regelsatzdatei zwar jederzeit bearbeiten, der Bildserver erkennt die Änderungen jedoch erst, wenn der zugehörige Materialkatalog neu geladen wird. Dies geschieht, wenn die [!DNL Platform Server] gestartet oder neu gestartet wird und wenn die primäre Katalogdatei (die das Suffix [!DNL .ini] aufweist) geändert oder „berührt“ wird (um das Dateidatum zu ändern).

## Beispiele {#section-c4142a41f5cd4ff799a72fbc130c3700}

Beispiele für Regelsätze finden Sie im entsprechenden Abschnitt der Image-Katalogreferenz in der Dokumentation zu Image-Serving.

## Verwandte Themen {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
