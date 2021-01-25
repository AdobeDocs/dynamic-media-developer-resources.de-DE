---
description: Das Image Rendering unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anforderungen, der auf Regeln für die Übereinstimmung und Ersetzung von regulären Ausdrücken basiert.
seo-description: Das Image Rendering unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anforderungen, der auf Regeln für die Übereinstimmung und Ersetzung von regulären Ausdrücken basiert.
seo-title: Regelsatz
solution: Experience Manager
title: Regelsatz
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# Regelsatzverweis{#rule-set-reference}

Das Image Rendering unterstützt einen einfachen Mechanismus zur Vorverarbeitung von Anforderungen, der auf Regeln für die Übereinstimmung und Ersetzung von regulären Ausdrücken basiert.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Sammlungen von Vorverarbeitungsregeln (*Regelsätze*) können an Materialkataloge oder den Standardkatalog angehängt werden. Regeln im Standardkatalog gelten nur, wenn die Anforderung keinen bestimmten Materialkatalog anfügt.

Vorverarbeitungsregeln für Anfragen können den Pfad und die Abfrage von Anforderungen ändern, bevor sie vom Anforderungsparser des Servers verarbeitet werden. Dazu gehören das Manipulieren des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um einige Katalogattribute zu konfigurieren und außer Kraft zu setzen sowie um den Dienst auf bestimmte Client-IP-Adressen zu beschränken.

Regelsätze werden als XML-Dokument-Dateien gespeichert. Der relative oder absolute Pfad der Regelsatzdatei muss in `attribute::RuleSetFile` angegeben werden.

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

Die Elemente `<?xml>`, `<!DOCTYPE>` und `<ruleset>` sind in einer gültigen XML-Regelsatzdatei immer erforderlich, auch wenn keine tatsächlichen Regeln definiert sind.

Ein `<ruleset>`-Element, das eine beliebige Anzahl von `<rule>`-Elementen enthält, ist zulässig.

Beim Inhalt von Regeldateien zur Vorverarbeitung wird die Groß-/Kleinschreibung beachtet.

## URL-Vorverarbeitung {#section-737a38d1b8c746f995e64fa6cfbcec87}

Vor jeder anderen Verarbeitung wird eine eingehende HTTP-Anforderung teilweise analysiert, um zu bestimmen, welcher Materialkatalog angewendet werden soll. Sobald der Katalog identifiziert wurde, wird der Regelsatz für den ausgewählten Katalog (oder der Standardkatalog, wenn kein bestimmter Katalog identifiziert wurde) angewendet.

Die `<rule>`-Elemente werden in der angegebenen Reihenfolge nach dem Inhalt des `<expression>`-Elements ( *`expression`*) gesucht.

Wenn eine `<rule>`-Übereinstimmung vorliegt, wird die optionale *`substitution`*-Zeichenfolge angewendet und die geänderte Anforderungs-Zeichenfolge wird zur normalen Verarbeitung an den Anforderungsparser des Servers übergeben.

Wenn beim Erreichen des Endes von `<ruleset>` keine erfolgreiche Übereinstimmung erfolgt, wird die Anforderung ohne Änderung an den Parser übergeben.

## Das OnMatch-Attribut {#section-7a8ad3597780486985af5e9a3b1c7b56}

Das Standardverhalten kann mit dem `OnMatch`-Attribut der `<rule>`-Elemente geändert werden. `OnMatch` kann auf  `break` (Standard),  `continue`oder  `error.`

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
   <td colname="col2"> <p>Die Regelverarbeitung wird unmittelbar nach der Anwendung der Ersetzung für diese Regel beendet. Standard. </p> </td> 
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

## Außerkraftsetzen von Katalogattributen {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` -Elemente können optional Attribute definieren, die die entsprechenden Katalogattribute außer Kraft setzen, wenn die Regel erfolgreich abgeglichen und festgelegt  `OnMatch="break"` wurde. Wenn `OnMatch="continue"` eingestellt ist, werden keine Attribute angewendet. Eine Liste von Attributen, die mit Regeln gesteuert werden können, finden Sie in der Beschreibung von `<rule>`.

## Reguläre Ausdruck {#section-4d326507b52544b0960a9a5f303e3fe6}

Einfache Zeichenfolgenübereinstimmung funktioniert bei sehr einfachen Anwendungen, in den meisten Fällen sind jedoch reguläre Ausdruck erforderlich. Während reguläre Ausdruck Branchenstandard sind, variiert die spezifische Implementierung von Instanz zu Instanz.

[package java.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regexbeschreibt die spezielle Implementierung des regulären Ausdrucks, die von Image Serving verwendet wird.

## Erfasste Teilzeichenfolgen {#section-8057cd65d48949ffb6a50e929bd3688b}

Um komplexe URL-Änderungen zu erleichtern, können Teilzeichenfolgen im Ausdruck erfasst werden, indem sie die Unterzeichenfolge mit Klammern (...) versehen. Erfasste Teilzeichenfolgen werden entsprechend der Position der führenden Klammer sequenziell mit 1 nummeriert. Die erfassten Teilzeichenfolgen können mit *`$n`* in die Ersetzung eingefügt werden, wobei *`n`* die Sequenznummer der erfassten Teilzeichenfolge ist.

## Verwalten von Regelsatzdateien {#section-e8ce976b56404c009496426fd334d23d}

Eine Regelsatzdatei kann mit dem Katalogattribut `attribute::RuleSetFile` an jeden Materialkatalog angehängt werden. Während Sie die Regelsatzdatei jederzeit bearbeiten können, erkennt der Image-Server die Änderungen nur, wenn der zugehörige Materialkatalog neu geladen wird. Dies geschieht, wenn der Plattformserver gestartet oder neu gestartet wird und die primäre Katalogdatei (die das Suffix [!DNL .ini] enthält) geändert oder &quot;angefasst&quot;wird (um das Dateidatum zu ändern).

## Beispiele {#section-c4142a41f5cd4ff799a72fbc130c3700}

Regelsatzbeispiele finden Sie im entsprechenden Abschnitt der Bildkatalog-Referenz in der Image Serving-Dokumentation.

## Verwandte Themen {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
