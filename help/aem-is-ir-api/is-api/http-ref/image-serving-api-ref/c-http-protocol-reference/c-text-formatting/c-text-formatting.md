---
description: Image Serving bietet mehrere Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.
solution: Experience Manager
title: Textformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 6%

---

# Textformatierung{#text-formatting}

Image Serving bietet mehrere Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.

`textPs=` bietet ein hohes Maß an Ähnlichkeit mit Text, der mit Adobe Photoshop und Illustrator gerendert wird. `text=` ist mit Text kompatibel, der mit Windows WordPad gerendert wird.

>[!NOTE]
>
>Zusätzlich zu den an anderer Stelle aufgeführten Unterschieden führt `text=` zu geringfügigen Unterschieden zwischen gerendertem Text und gerendertem Text im Vergleich zu `textPs=`. Beispielsweise haben Unterstriche nicht die gleiche Dicke und Position und synthetisierte Kursivformatierungen werden in einem etwas anderen Winkel gerendert. Wenn Text nicht in den verfügbaren Platz passt, schneidet `text=` die letzte Zeile möglicherweise teilweise ab, während `textPs=` nur vollständige Zeilen rendert.

Alle Textbefehle akzeptieren formatierten Text, der auf einer Teilmenge der RTF-Spezifikation (Rich Text Format) basiert. Jede Textebene kann einen anderen Textbefehl angeben.

In der folgenden Tabelle sind die wichtigsten Funktionen aufgeführt, die für jeden Textbefehl verfügbar sind:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Funktion</b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Siehe auch</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop-kompatibel </p> </td> 
   <td> <p> nein </p> </td> 
   <td> <p> begrenzt </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text in beliebige Formen fließen </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text entlang beliebiger Pfade fließen </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Einpassung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Kopienanpassung <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ränder von Textfeldern </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\Margl</pre>, <pre>\Margr</pre>, <pre>\mrgt</pre>, <pre>\margin</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Vollständige Absatzbegründung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Letzte Zeilenausrichtung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Absatzeinzug </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text mit Kapitälchen und Kapitälchen </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Bildbereitstellungsfarben </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\*\isColorTbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mehrere Anti-Aliasing-Modi </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfluss von oben nach unten/rechts nach links </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fotofont®-Unterstützung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Schriftverarbeitung </td> 
  </tr> 
  <tr> 
   <td> <p>Ebene automatisch an Text anpassen </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK-Unterstützung </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\CMYKCOLORTBL, \*\isColorTBL </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Rechts-nach-links-Zeichenfluss </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Zeilenumbruch deaktivieren </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text automatisch skalieren, um Ebene anzupassen (durch unterschiedliche Auflösung) </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF-konforme Zeichenfolgen können manuell oder durch Formatieren des gewünschten Textes in einem Texteditor oder Textprozessor zusammengestellt werden, der RTF-Dateien speichern kann. Die RTF-Datei kann dann in einem Texteditor geöffnet werden, und der entsprechende rohe RTF-Inhalt der Datei kann in die Anfrage-URL kopiert werden.

Einige Textverarbeitungssysteme generieren recht große Dateien, die umfangreiche Präambeln enthalten, die von Dynamic Media Image Serving nicht verwendet werden. Es wird empfohlen, die nicht verwendeten RTF-Elemente aus der Zeichenfolge zu entfernen, bevor die Zeichenfolge an die Textbefehle übergeben wird.

Sprachkodierung basierend auf UTF-8- und ISO-Standards wird in RTF-Zeichenfolgen als Alternative zu den standardmäßigen RTF-Zeichenkodierungsmechanismen unterstützt. Dadurch können Anwendungen nicht-englischen Text ohne Kenntnisse der RTF-Kodierung an den Server senden.

Alle nicht HTTP-konformen Zeichen müssen ordnungsgemäß maskiert sein, wenn die Zeichenfolge über HTTP übertragen werden soll. Nur &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; müssen maskiert werden, wenn die Zeichenfolge in das `catalog::Modifiers` Feld eines Bildkatalogdatensatzes integriert ist. Steuerzeichen wie `<CR>`, `<LF>` und `<TAB>` sollten immer entfernt werden.

Die Image-Serving-Text-Engines interpretieren eine Untergruppe von Befehlen, die in der Rich-Text-Format-Spezifikation (RTF), Version 1.6, definiert sind. Diese Untergruppe konzentriert sich auf die Schriftart-/Zeichenformatierung, die einfache Absatzformatierung und die Unterstützung internationaler Schriftarten und Zeichensätze. Erweiterte Formatierungskonstrukte wie Stylesheets und Tabellen werden derzeit nicht unterstützt.

Wenn Sie versuchen, RTF-kodierte Textzeichenfolgen manuell zu erstellen, müssen Sie mit der von Microsoft veröffentlichten Rich-Text-Format-Spezifikation (RTF) vertraut sein.

* [Schriftbehandlung](r-font-handling.md)
* [Farbverarbeitung](r-color-handling.md)
* [Einpassung](r-copy-fitting.md)
* [Textebenen](r-text-layers.md)
* [Textpositionierung](r-text-positioning.md)
* [Reservierte Zeichen](r-reserved-characters.md)
* [Unterstützte RTF-Befehle und -Schlüsselwörter](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Beispiele für RTF-Kodierung](r-rtf-encoding-examples.md)
