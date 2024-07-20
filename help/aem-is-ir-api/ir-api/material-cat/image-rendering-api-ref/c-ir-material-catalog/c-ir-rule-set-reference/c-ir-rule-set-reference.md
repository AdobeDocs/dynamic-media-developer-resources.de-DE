---
description: Das Bild-Rendering unterstützt einen einfachen Anfragevorverarbeitungsmechanismus, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.
solution: Experience Manager
title: Regelsatzreferenz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Regelsatzreferenz{#rule-set-reference}

Das Bild-Rendering unterstützt einen einfachen Anfragevorverarbeitungsmechanismus, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Sammlungen von Vorab-Verarbeitungsregeln (*Regelsätze*) können an Materialkataloge oder den Standardkatalog angehängt werden. Regeln im Standardkatalog gelten nur, wenn die Anfrage keinen bestimmten Materialkatalog anfügt.

Vorab-Verarbeitungsregeln für Anfragen können den Pfad und die Anfrageabschnitte von Anforderungen ändern, bevor sie vom Anforderungsparser des Servers verarbeitet werden. Dazu gehören das Manipulieren des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um einige Katalogattribute zu konfigurieren und zu überschreiben sowie um den Dienst auf bestimmte Client-IP-Adressen zu beschränken.

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

Die Elemente `<?xml>`, `<!DOCTYPE>` und `<ruleset>` sind immer in einer gültigen XML-Regelsatzdatei erforderlich, selbst wenn keine tatsächlichen Regeln definiert sind.

Ein `<ruleset>` -Element, das eine beliebige Anzahl von `<rule>` -Elementen enthält, ist zulässig.

Beim Inhalt von Regeldateien zur Vorverarbeitung wird zwischen Groß- und Kleinschreibung unterschieden.

## URL-Vorverarbeitung {#section-737a38d1b8c746f995e64fa6cfbcec87}

Vor jeder anderen Verarbeitung wird eine eingehende HTTP-Anforderung teilweise analysiert, um zu bestimmen, welcher Materialkatalog angewendet werden soll. Sobald der Katalog identifiziert wurde, wird der Regelsatz für den ausgewählten Katalog (oder der Standardkatalog, wenn kein bestimmter Katalog identifiziert wurde) angewendet.

Die Elemente `<rule>` werden in der Reihenfolge gesucht, die für eine Übereinstimmung mit dem Inhalt des Elements `<expression>` ( *`expression`*) angegeben ist.

Wenn eine `<rule>` -Übereinstimmung vorliegt, wird das optionale *`substitution`* angewendet und die geänderte Anforderungszeichenfolge wird zur normalen Verarbeitung an den Anforderungsparser des Servers übergeben.

Wenn beim Erreichen des Endes von `<ruleset>` keine erfolgreiche Übereinstimmung erfolgt, wird die Anforderung ohne Änderung an den Parser übergeben.

## Das OnMatch-Attribut {#section-7a8ad3597780486985af5e9a3b1c7b56}

Das Standardverhalten kann mit dem Attribut `OnMatch` der Elemente `<rule>` geändert werden. `OnMatch` kann auf `break` (Standard), `continue` oder `error.` gesetzt werden

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element und Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Verhalten bei Übereinstimmung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Die Regelverarbeitung wird sofort beendet, nachdem die Ersetzung für diese Regel vorgenommen wurde. Standard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Die Ersetzung wird angewendet und die Verarbeitung wird mit der nächsten Regel fortgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Die Regelverarbeitung wird sofort beendet und der Antwortstatus "Anfrage verweigert"wird an den Client zurückgegeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Überschreiben von Katalogattributen {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` -Elemente können optional Attribute definieren, die die entsprechenden Katalogattribute überschreiben, wenn die Regel erfolgreich übereinstimmt und `OnMatch="break"` festgelegt ist. Wenn `OnMatch="continue"` festgelegt ist, werden keine Attribute angewendet. Eine Liste der Attribute, die mit Regeln gesteuert werden können, finden Sie in der Beschreibung von `<rule>` .

## Reguläre Ausdrücke {#section-4d326507b52544b0960a9a5f303e3fe6}

Einfache Zeichenfolgenabgleiche funktionieren für sehr einfache Anwendungen, aber in den meisten Fällen sind reguläre Ausdrücke erforderlich. Während reguläre Ausdrücke den Branchenstandard aufweisen, variiert die spezifische Implementierung von Instanz zu Instanz.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beschreibt die spezifische Implementierung des regulären Ausdrucks, die von Image Serving verwendet wird.

## Erfasste Unterzeichenfolgen {#section-8057cd65d48949ffb6a50e929bd3688b}

Um komplexe URL-Änderungen zu erleichtern, können Unterzeichenfolgen im Ausdruck erfasst werden, indem die Unterzeichenfolge in Klammern (...) eingeschlossen wird. Erfasste Teilzeichenfolgen werden in der Reihenfolge mit 1 beginnend gemäß der Position der führenden Klammer nummeriert. Die erfassten Teilzeichenfolgen können mit *`$n`* in die Substitution eingefügt werden, wobei *`n`* die Sequenznummer der erfassten Teilzeichenfolge ist.

## Verwalten von Regelsatzdateien {#section-e8ce976b56404c009496426fd334d23d}

An jeden Materialkatalog mit dem Katalogattribut `attribute::RuleSetFile` kann eine Regelsatzdatei angehängt werden. Sie können die Regelsatzdatei zwar jederzeit bearbeiten, der Bildserver erkennt die Änderungen jedoch nur, wenn der verknüpfte Materialkatalog neu geladen wird. Dies geschieht, wenn der [!DNL Platform Server] -Befehl gestartet oder neu gestartet wird und die primäre Katalogdatei (die das Suffix [!DNL .ini] aufweist) geändert oder &quot;berührt&quot; wird (um das Dateidatum zu ändern).

## Beispiele {#section-c4142a41f5cd4ff799a72fbc130c3700}

Regelsatzbeispiele werden im entsprechenden Abschnitt der Bildkatalog-Referenz in der Image Serving-Dokumentation bereitgestellt.

## Verwandte Themen {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
