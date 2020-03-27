---
description: Image Serving bietet mehrere Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.
seo-description: Image Serving bietet mehrere Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.
seo-title: Textformatierung
solution: Experience Manager
title: Textformatierung
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Textformatierung{#text-formatting}

Image Serving bietet mehrere Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.

`textPs=` bietet eine hohe Ähnlichkeit mit Text, der mit Adobe Fotoshop und Illustrator gerendert wird. `text=` ist mit Text, der mit Windows Wordpad gerendert wird, relativ kompatibel.

>[!NOTE]
>
>Zusätzlich zu den an anderer Stelle aufgeführten Unterschieden `text=` entstehen im gerenderten Text geringfügige Unterschiede im Vergleich zu `textPs=`. Beispielsweise haben die Unterstriche nicht dieselbe Dicke und Position und die Kursivformatierung wird in einem etwas anderen Winkel dargestellt. Wenn der Text nicht in den verfügbaren Platz passt, `text=` kann die letzte Zeile teilweise beschnitten werden, während nur vollständige Zeilen gerendert `textPs=` werden.

Alle Textbefehle akzeptieren formatierten Text, der auf einer Untergruppe der RTF-Spezifikation (Rich Text Format) basiert. Jede Textebene kann einen anderen Textbefehl angeben.

In der folgenden Tabelle werden die wichtigsten Funktionen für jeden Textbefehl Liste:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Funktion</b> </th> 
   <th class="entry"> <b> Text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Verwandte Themen</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Fotoshop-kompatibel </p> </td> 
   <td> <p> nein </p> </td> 
   <td> <p> begrenzt </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfluss in beliebige Formen </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfluss entlang beliebiger Pfade </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Kopiereinpassung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Copy-Fitting <p>, \copyfit, \copyfitlines, \copyfitmaxlines </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfeldränder </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\margl, \margr, \margt, \margb </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Vollständige Absatzausrichtung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\qj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>letzte Zeile </p> </td> 
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
   <td> <p>Großbuchstaben- und Kleinbuchstabentext </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Image Serving-Farben </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mehrere Glättungsmodi </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfluss oben unten/rechts </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fotofont®-Unterstützung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Schrift-Handhabung </td> 
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
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfluss von rechts nach links </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Wortumbruch deaktivieren </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text automatisch an die jeweilige Ebene anpassen (durch unterschiedliche Auflösung) </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF-konforme Zeichenfolgen können manuell oder durch Formatierung des gewünschten Textes in einem Texteditor oder Textverarbeitungsprogramm, der RTF-Dateien speichern kann, zusammengestellt werden. Die RTF-Datei kann dann in einem Texteditor geöffnet und der relevante RTF-Rohinhalt der Datei in die Anforderungs-URL kopiert werden.

Einige Textverarbeitungen erzeugen ziemlich große Dateien, die umfangreiche Präambel enthalten, die nicht von Scene7 Image Serving verwendet werden. Es wird empfohlen, die nicht verwendeten RTF-Elemente aus der Zeichenfolge zu entfernen, bevor die Zeichenfolge an die Textbefehle übergeben wird.

Die Sprachkodierung auf Basis von UTF-8- und ISO-Standards wird in RTF-Zeichenfolgen als Alternative zu den Standard-RTF-Zeichenkodierungsmechanismen unterstützt. Dadurch können Anwendungen nicht-englischsprachigen Text ohne Kenntnisse der RTF-Kodierung an den Server senden.

Alle nicht HTTP-konformen Zeichen müssen mit einem korrekten Escape versehen werden, wenn die Zeichenfolge über HTTP übertragen werden soll. Nur &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; müssen mit Escape-Zeichen versehen werden, wenn die Zeichenfolge in das `catalog::Modifiers` Feld eines Bildkatalogdatensatzes eingebunden ist. Steuerzeichen einschließlich `<CR>`, `<LF>``<TAB>` und sollten immer entfernt werden.

Die Image Serving-Textmaschinen interpretieren einen Teil der Befehle, die in der RTF-Spezifikation, Version 1.6, definiert sind. Diese Untergruppe konzentriert sich auf die Schriftart-/Zeichenformatierung, die einfache Absatzformatierung und die Unterstützung für internationale Schriftarten und Zeichensätze. Erweiterte Formatierungskonstrukte wie Stylesheets und Tabellen werden derzeit nicht unterstützt.

Die Kenntnis der RTF-Spezifikation (Rich Text Format), wie sie von Microsoft veröffentlicht wurde, ist erforderlich, wenn versucht wird, RTF-kodierte Textzeichenfolgen manuell zu erstellen.

* [Schriftverarbeitung](r-font-handling.md)
* [Farbhandhabung](r-color-handling.md)
* [Kopiereinpassung](r-copy-fitting.md)
* [Textebenen](r-text-layers.md)
* [Textpositionierung](r-text-positioning.md)
* [Reservierte Zeichen](r-reserved-characters.md)
* [Unterstützte RTF-Befehle und -Suchbegriffe](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF-Kodierungsbeispiele](r-rtf-encoding-examples.md)
