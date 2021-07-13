---
description: Image Serving bietet verschiedene Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.
solution: Experience Manager
title: Textformatierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 7%

---

# Textformatierung{#text-formatting}

Image Serving bietet verschiedene Alternativen zum Rendern von Text, auf die mit den Befehlen text= und textPs= zugegriffen werden kann.

`textPs=` bietet eine hohe Ähnlichkeit mit in Adobe Photoshop und Illustrator gerendertem Text. `text=` ist mit Text kompatibel, der mit Windows Wordpad gerendert wird.

>[!NOTE]
>
>Zusätzlich zu den an anderer Stelle aufgeführten Unterschieden führt `text=` zu geringfügigen Unterschieden im gerenderten Text im Vergleich zu `textPs=`. So weisen beispielsweise Unterstriche nicht die gleiche Dicke und Position auf und werden kursiv synthetisiert und in einem etwas anderen Winkel gerendert. Wenn der Text nicht in den verfügbaren Bereich passt, kann `text=` die letzte Zeile teilweise zuschneiden, während `textPs=` nur vollständige Zeilen rendert.

Alle Textbefehle akzeptieren formatierten Text basierend auf einer Teilmenge der RTF-Spezifikation (Rich Text Format). Jede Textebene kann einen anderen Textbefehl angeben.

In der folgenden Tabelle sind die wichtigsten Funktionen aufgeführt, die für jeden Textbefehl verfügbar sind:

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
   <td> <p> Adobe Photoshop-kompatibel </p> </td> 
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
   <td> <p>Nachrüstung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Copy-Fitting <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfeldränder </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Vollständige Absatzdarstellung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Letzte Zeile - Begründung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Absatzeinrückung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text mit Großbuchstaben und Kleinbuchstaben </p> </td> 
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
   <td> <p>Mehrere Anti-Aliasing-Modi </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textfluss oben unten/rechts links </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fotofont®-Unterstützung </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Schrifthandhabung </td> 
  </tr> 
  <tr> 
   <td> <p>Ebene automatisch an Textgröße anpassen </p> </td> 
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
   <td> <p>Zeichenfluss von rechts nach links </p> </td> 
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
   <td> <p>Text automatisch an die Ebene anpassen (durch variierende Auflösung) </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>nein </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF-konforme Zeichenfolgen können manuell oder durch Formatierung des gewünschten Textes in einem Texteditor oder Textverarbeitungsprogramm zusammengestellt werden, der RTF-Dateien speichern kann. Die RTF-Datei kann dann in einem Texteditor geöffnet werden und der relevante RTF-Rohinhalt der Datei wird in die Anfrage-URL kopiert.

Einige Textverarbeitungen erzeugen recht große Dateien, die wesentliche Präambel enthalten, die nicht von Dynamic Media Image Serving verwendet werden. Es wird empfohlen, die nicht verwendeten RTF-Elemente aus der Zeichenfolge zu entfernen, bevor die Zeichenfolge an die Textbefehle übergeben wird.

Sprachkodierung basierend auf UTF-8- und ISO-Standards wird in RTF-Zeichenfolgen als Alternative zu den Standard-RTF-Zeichenkodierungsmechanismen unterstützt. Dadurch können Anwendungen nicht-englischsprachigen Text ohne Kenntnisse der RTF-Kodierung an den Server senden.

Alle nicht HTTP-konformen Zeichen müssen ordnungsgemäß maskiert sein, wenn die Zeichenfolge über HTTP übertragen werden soll. Nur &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; müssen maskiert werden, wenn die Zeichenfolge in das Feld `catalog::Modifiers` eines Bildkatalogdatensatzes integriert ist. Kontrollzeichen wie `<CR>`, `<LF>` und `<TAB>` sollten immer entfernt werden.

Die Image Serving Text Engines interpretieren eine Untergruppe von Befehlen, die durch die RTF-Spezifikation (Rich Text Format), Version 1.6 definiert werden. Diese Untergruppe konzentriert sich auf die Schriftart-/Zeichenformatierung, einfache Absatzformatierung und die Unterstützung für internationale Schriftarten und Zeichensätze. Erweiterte Formatierungskonstrukte wie Stylesheets und Tabellen werden derzeit nicht unterstützt.

Wenn Sie versuchen, RTF-kodierte Textzeichenfolgen manuell zu erstellen, müssen Sie mit der von Microsoft veröffentlichten Rich Text Format (RTF)-Spezifikation vertraut sein.

* [Schriftverarbeitung](r-font-handling.md)
* [Farbhandhabung](r-color-handling.md)
* [Nachrüstung](r-copy-fitting.md)
* [Textebenen](r-text-layers.md)
* [Textpositionierung](r-text-positioning.md)
* [Reservierte Zeichen](r-reserved-characters.md)
* [Unterstützte RTF-Befehle und Keywords](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF-Kodierungsbeispiele](r-rtf-encoding-examples.md)
