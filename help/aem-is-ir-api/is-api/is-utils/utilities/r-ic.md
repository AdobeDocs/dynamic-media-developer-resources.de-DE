---
description: Dienstprogramm zur Bildkonvertierung.
solution: Experience Manager
title: IC
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# IC {#ic}

Dienstprogramm zur Bildkonvertierung.

`ic` ist ein Befehlszeilen-Tool, das Bilddateien in das optimierte Pyramid TIFF-Format (PTIFF) konvertiert. Obwohl die Bildbereitstellung Bilder ohne Konvertierung verarbeiten kann, empfehlen wir, alle Bilder mit einer Größe von mehr als 512 x 512 Pixel in PTIFF zu konvertieren. Diese Konvertierung sorgt für eine optimale Server-Leistung und Ressourcennutzung und minimiert die Reaktionszeiten.

Es wird empfohlen, PTIFF-Dateien, die fotografischen Inhalt enthalten, mit JPEG zu codieren (geben Sie `-jpegcompress` an). Computergenerierte Inhalte können von der verlustfreien Komprimierung profitieren (entweder `-deflatecompress` oder `-lzwcompress`). Sofern keine Farbkonvertierung oder Pixeltypkonvertierung erforderlich ist, werden JPEG-Quellbilddaten ohne Decodierung auf PTIFF übertragen, um eine Qualitätsverschlechterung zu vermeiden. In diesem Fall gelten die angegebenen Komprimierungsoptionen nur für die Pyramidenebenen mit niedrigerer Auflösung.

Wenn Sie keine großen Bilder konvertieren, müssen Sie nicht die Parameter festlegen, die steuern, wie viel Speicher verwendet werden soll. Falls doch, geben Sie `ic` mehr Speicher, indem Sie die unten beschriebene `-maxmem` verwenden. Eine gute Faustregel für die Berechnung der benötigten Speichermenge ist die Multiplikation der Breite des Bildes mit der Höhe des Bildes mit der Anzahl der Kanäle. Beispiel: vier für ein RGB-Bild mit der dreifachen Alpha-Rate. Außerdem, wenn die Kanäle 16-Bit pro Komponente statt 8 doppelt so groß sind wie das Endergebnis.

## Nutzung {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>Optionen</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Befehlsoptionen (siehe unten). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Einzelne Eingabebilddatei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Einzelne PTIFF-Ausgabedatei (bei Verwendung mit SourceDirectory nicht gültig). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Ordner mit den Eingabebildern </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Ordner, in den die PTIFF-Ausgabedateien geschrieben werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-36a2dcfa39824d29b69547c432366219}

0 bei Erfolg. Wenn ein Fehler auftritt, wird ein Wert ungleich null zurückgegeben und Fehlerdetails werden an `stderr` gesendet.

## Optionen {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - unkomprimierte </span> </p> </td> 
   <td colname="col2"> <p>Das Ausgabebild wird nicht komprimiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Deflate-Komprimierung (ZIP) verwenden (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Lempel-Ziv-Welch-Komprimierung (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG-Kodierung verwenden. Ignoriert, wenn <span class="codeph"> <span class="varname"> sourceFile </span> </span> Alpha-Daten enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -JpegQuality &lt; <span class="varname"> Quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG-Qualität (0-100; Standard ist 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-fullSampleChrominance-</span> </p> </td> 
   <td colname="col2"> <p>JPEG-Chroma-Downsampling deaktivieren (kann die Qualität von Farbtext und Grafiken verbessern). Dies hat keine Auswirkungen auf Ausgabebilder, die CMYK oder Graustufen aufweisen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> Betrag </span>&gt; &lt; <span class="varname"> Radius </span>&gt; &lt; <span class="varname"> Schwellenwert </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Unschärfemaske auf untergeordnete Pyramidenebenen anwenden. Weitere Informationen finden Sie unter <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> . (Nicht auf das Bild mit voller Auflösung angewendet.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath-</span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie den Clip-Pfad in der Quelldatei, falls vorhanden, um verknüpfte Alpha-Daten zu erstellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Druckauflösung (dpi) für <span class="codeph"> <span class="varname"> destFile </span> </span>; wenn nicht angegeben, wird die Druckauflösung <span class="codeph"> srcFile-</span> in <span class="codeph"> <span class="varname"> destFile </span> </span> kopiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -automatisches Zuschneiden &lt; <span class="varname"> Ecke </span>&gt; &lt; <span class="varname"> Modus </span>&gt; &lt; <span class="varname"> Toleranz </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Berechnen Sie ein Zuschnittsrechteck, um einen einfarbigen Hintergrund zu minimieren. Es werden keine Zuschnittsinformationen ausgegeben, wenn der Algorithmus für das automatische Zuschneiden dazu führen würde, dass das gesamte Bild abgeschnitten wird. </p> <p>Um das Zuschnittsrechteck ohne Konvertierung des Bildes zu berechnen, geben Sie <span class="codeph"> -</span> ohne <span class="codeph"> -convert </span> und ohne <span class="codeph"> <span class="varname"> destFile.</span> an</span></p>

<p><i><b>Ecke</b></i> - ul | UR | LL | LR </p>
   <p> Gibt an, welche Bildecke einen Startpunkt verwenden soll. Ignoriert, wenn der Modus 1 ist.</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>Auf 0 gesetzt, um basierend auf der Farbe des angegebenen Eckpixel zuzuschneiden; arbeitet mit vormultiplizierten Farbdaten, wenn dem Quellbild Alpha-Daten zugeordnet sind.</p>
   <p>Auf 1 gesetzt, um basierend auf Alpha-Daten zuzuschneiden; Ecke wird ignoriert und 0 ist immer der Seed-Wert; es wird kein Zuschnitt angewendet, wenn dem Quellbild keine Alpha-Daten zugeordnet sind.</p> 
   <p><i><b>Toleranz</b></i> - Toleranz anpassen. Realer Wert 0,0 bis 1,0. Gibt die Toleranz für übereinstimmende Pixelkomponentenwerte an. Auf 0 für exakte Übereinstimmungen festlegen.</p>
   <p><i><b>infoFile</b></i> - Pfad und Name der XML-Ausgabedatei, in die die Zuschnittinformationen geschrieben werden.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData-</span> </p> </td> 
   <td colname="col2"> <p>Kopieren Sie XMP-Metadaten, falls verfügbar, aus <span class="codeph"> <span class="varname"> sourceFile </span> </span> ohne Änderung in <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile-</span> </p> </td> 
   <td colname="col2"> <p> Einbetten des ICC-Farbprofils in <span class="codeph"> <span class="varname"> destFile </span> </span>, falls verfügbar (standardmäßig ist kein Profil eingebettet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name einer ICC-Profildatei. Definiert den Farbraum <span class="codeph"> <span class="varname"> sourceFile </span> </span> und muss mit dem Pixeltyp übereinstimmen. Sollte nur angegeben werden, wenn kein Profil in <span class="codeph"> <span class="varname">-Quelldatei </span> </span> eingebettet ist, da dies das eingebettete Profil überschreibt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name einer ICC-Profildatei. Definiert den Pixeltyp und Farbraum <span class="codeph"> <span class="varname"> destFile </span> </span>. IC konvertiert in dieses Profil, wenn <span class="codeph"> <span class="varname">-Quelldatei </span> </span> ein eingebettetes Profil hat oder wenn auch <span class="codeph"> -</span> angegeben ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Perzeptive Render-Absicht für Farbraumkonversionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric-</span> </p> </td> 
   <td colname="col2"> <p> Relative farbmetrische Render-Absicht für Farbraumkonvertierungen (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric-</span> </p> </td> 
   <td colname="col2"> <p>Absoluter farbmetrischer Rendering-Intent für Farbraumkonversionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation-</span> </p> </td> 
   <td colname="col2"> <p>Render Intent für Sättigung für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation-</span> </p> </td> 
   <td colname="col2"> <p>Blackpoint-Kompensation für bestimmte Farbkonvertierungen deaktivieren </p> <p>Standardmäßig aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie Dithering (Fehlerdiffusion) bei der Farbkonvertierung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -retainPixelType </span> </p> </td> 
   <td colname="col2"> <p> Automatische Konvertierung von CMYK in RGB deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress-</span> </p> </td> 
   <td colname="col2"> <p>Dekodierung und Neukodierung von JPEG-Eingabebildern erzwingen. </p> <p> <b>Achtung:</b> diese Option kann die Bildqualität beeinträchtigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen (bilinearen) Resampling-Filter mit Standardqualität. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Neuberechnungsfilter mit höherer Qualität (Lanczos-Fenster) (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Filter für das erneute Sampling mit höherer Qualität (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Downsample mit Photoshop Style 8x8 bikubisch-scharfer Filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Wenn als erste Option angegeben, unterdrückt die Ausgabe von Nutzungsinformationen, wenn ungültige Optionen gefunden werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - </span> überschreiben </p> </td> 
   <td colname="col2"> <p>Überschreiben einer vorhandenen <span class="codeph"> <span class="varname"> destFile </span> </span> zulassen. Standardmäßig wird ein numerisches Suffix an den Dateinamen angehängt, um das Überschreiben zu verhindern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ausgeblendete Quelldateien ignorieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueOnError </span> </p> </td> 
   <td colname="col2"> <p>Beenden Sie die Verarbeitung nicht, wenn ein Fehler auftritt. Wirkt sich nur aus, wenn mehrere Dateien verarbeitet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name der Protokolldatei (standardmäßig <span class="codeph"> stdout-</span>) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logLevel &lt; <span class="varname"> Level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Protokollebene. </p> 
   <p>&lt; 0 - Protokollierung deaktiviert.</p>
   <p>0 - Listet die zu verarbeitenden Dateien auf.</p>
   <p>1. Hinzufügen von Berichten für nicht benötigte Dateien.</p>
   <p>2. Hinzufügen von Fortschrittsberichten.</p>
   <p>3. Fügen Sie Berichte zu jeder gefundenen Datei hinzu.</p>
   <p>4. Hinzufügen von Fortschrittsberichten auf Dateiebene.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>An Protokolldatei anhängen (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Protokolldatei überschreiben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logProgressMsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Protokollierungsintervall in ms für Protokollebene 2 und höher (Standard ist 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxMem &lt; <span class="varname"> Bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Speicherbeanspruchungsgrenze. Muss mindestens 10 MB groß sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxMemPercent &lt; <span class="varname"> Percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Speicherbeanspruchungsgrenze. Der Standardwert beträgt 25 % des physischen Speichers. Wenn weder <span class="codeph"> maxmem-</span> noch <span class="codeph"> maxmempercent-</span> explizit festgelegt sind, wird standardmäßig maxmempercent verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne andere Optionen an. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Unterstützte Eingabebildformate {#section-ab13d941d6724e65b9f84b62d949d31c}

In der folgenden Tabelle sind die Bilddateiformate und Formatoptionen aufgeführt, die von IC unterstützt werden.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel-Typ</b> <b> Bits/Kette</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Kette</b> </p> </th> 
   <th class="entry"> <p> <b> Komprimierung</b> </p> </th> 
   <th class="entry"> <p> <b> Anmerkungen</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows-Bitmap) </p> </td> 
   <td> <p> RGB | indiziert </p> </td> 
   <td> <p> 1 | 05/6 | 8 </p> </td> 
   <td> <p> unkomprimiert | ROLLE </p> </td> 
   <td> <p> 5/6 bit/channel bedeutet Unterstützung für 16-bit RGB (5-5-5 und 5-6-5 bit/channel). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated PostScript) </p> </td> 
   <td> <p> CMYK | RGB | grau </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binär | JPEG </p> </td> 
   <td> <p> Es werden nur von Photoshop generierte EPS-Dateien unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indiziert </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> GESETZ </p> </td> 
   <td> <p> Falls vorhanden, wird der Transparenzwert in der Palette in Alpha umgewandelt. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | grau </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grau | grauA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> unkomprimiert | komprimiert </p> </td> 
   <td> <p> Nur zusammengeführtes Bild. Ebenen und zusätzliche Kanäle werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ROLLE </p> </td> 
   <td> <p> Nur Bitmap-Daten, Vektordaten werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | grau | grauA | indiziert </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> komprimiert </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grau | grauA | indiziert </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> unkomprimiert | PLZ | GESETZ | JPEG | CITT-REGEL | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> Mit Ausnahme des ersten zugehörigen Alphakanals werden zusätzliche Kanäle ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

Eingebettete ICC-Profile werden in EPS-, JPG-, PSD-, PNG- und TIFF-Dateien erkannt.

Eingebettete Pfade und XMP-Metadaten werden in EPS-, JPG-, PSD- und TIFF-Dateien erkannt.

## Beispiele {#section-3c1986b30315431989bd76b1ee5bef6d}

Konvertieren Sie ein einzelnes Bild in der besten Qualität und behalten Sie es im selben Ordner:

`ic -convert src/myFile.png src/myFile.tif`

Konvertieren Sie alle Bilder in *`srcFolder`* in JPEG-kodierte Pyramiden-TIFF und platzieren Sie sie in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Konvertieren Sie alle Bilder in *`srcFolder`*. Die kodierten Bilddaten von JPG-Dateien werden für die verlustfreie LZW-Komprimierung der Vollauflösungsstufe für die übrige Bildpyramide dieser Bilder sowie für das gesamte Ausgabebild aller Nicht-JPG-Eingabedateien verwendet. Die Pixeltypen, eingebetteten Farbprofile, XMP-Metadaten usw. gepflegt werden.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
