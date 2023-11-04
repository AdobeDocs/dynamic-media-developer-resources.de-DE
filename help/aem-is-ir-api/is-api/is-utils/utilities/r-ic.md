---
description: Bildkonvertierungsdienstprogramm.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 1%

---

# ic {#ic}

Bildkonvertierungsdienstprogramm.

`ic` ist ein Befehlszeilen-Tool, das Bilddateien in das optimierte Pyramid TIFF-Format (PTIFF) konvertiert. Image Serving kann zwar Bilder ohne Konvertierung verarbeiten, es wird jedoch empfohlen, alle Bilder, die größer als 512 x 512 Pixel sind, in PTIFF zu konvertieren. Diese Konvertierung sorgt für optimale Serverleistung und Ressourcenauslastung und minimiert die Reaktionszeiten.

Es wird empfohlen, PTIFF-Dateien, die fotografische Inhalte enthalten, JPEG-kodiert zu haben (geben Sie `-jpegcompress`). Computergenerierte Inhalte können von verlustfreier Komprimierung profitieren (entweder `-deflatecompress` oder `-lzwcompress`). Sofern keine Farbkonvertierung oder Pixeltypkonvertierung erforderlich ist, werden die JPEG-Quellbilddaten ohne Dekodierung in das PTIFF-Format übertragen, um eine Qualitätsminderung zu vermeiden. In diesem Fall gelten die angegebenen Komprimierungsoptionen nur für die Pyramidenebenen mit niedrigerer Auflösung.

Wenn Sie keine großen Bilder konvertieren, müssen Sie nicht die Parameter festlegen, die steuern, wie viel Speicher Sie verwenden. Wenn Sie dies jedoch tun, geben Sie `ic` mehr Speicher durch Verwendung von `-maxmem` unten beschrieben. Eine gute Faustregel für die Berechnung der erforderlichen Speichermenge besteht darin, die Breite des Bilds zu multiplizieren, um die Höhe des Bildes mit der Anzahl der Kanäle zu multiplizieren. Beispiel: Vier für ein RGB-Bild mit dem Alphakanal mal drei. Darüber hinaus, wenn die Kanäle 16 Bit pro Komponente statt 8 Bit sind das finale Ergebnis.

## Nutzung {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
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
   <td colname="col2"> <p>Ordner mit Eingabebildern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Ordner, in den die PTIFF-Ausgabedateien geschrieben werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-36a2dcfa39824d29b69547c432366219}

0 bei Erfolg. Wenn ein Fehler auftritt, wird ein Wert ungleich null zurückgegeben und Fehlerdetails werden an `stderr`.

## Optionen {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nicht komprimiert </span> </p> </td> 
   <td colname="col2"> <p>Komprimieren Sie das Ausgabebild nicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Komprimierung deflate (zip) (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Lempel-Ziv-Welch-Komprimierung (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie JPEG-Codierung. Ignoriert , wenn <span class="codeph"> <span class="varname"> sourceFile </span> </span> enthält Alpha-Daten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> Qualität </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG-Qualität (0-100; Standardwert ist 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominanz </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie das JPEG-Chroma-Downsampling (kann die Qualität des Farbtextes und der Grafiken verbessern). Dies hat keine Auswirkungen auf Ausgabebilder, die CMYK oder Graustufen sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> Schwellenwert </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Anwenden von Unschärfemaske auf subgesampelte Pyramidenebenen. Siehe <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> für Details. (Nicht auf das Bild mit voller Auflösung angewendet.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie gegebenenfalls den Pfad zum Clip in der Quelldatei, um die zugehörigen Alphataten zu erstellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Druckauflösung (dpi) für <span class="codeph"> <span class="varname"> destFile </span> </span>; falls nicht angegeben, die Druckauflösung von <span class="codeph"> srcFile </span> wird kopiert nach <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> Toleranz </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Berechnen Sie ein Zuschnittrechteck, um einen einfarbigen Hintergrund zu minimieren. Es werden keine Zuschnittinformationen ausgegeben, wenn der Algorithmus für das automatische Zuschneiden dazu führt, dass das gesamte Bild beschnitten wird. </p> <p>Um das Zuschnittrechteck zu berechnen, ohne das Bild zu konvertieren, geben Sie <span class="codeph"> -autocrop </span> without <span class="codeph"> -convert </span> und ohne <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i> - ul | EUR | ll | lr </p>
   <p> Gibt an, in welcher Ecke des Bildes ein Seed-Punkt verwendet werden soll. Wird ignoriert, wenn der Modus 1 ist.</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>Auf 0 setzen, um basierend auf der Farbe des angegebenen Ecke-Pixels zuzuschneiden. Funktioniert mit vormultiplizierten Farbdaten, wenn Alphatedaten mit dem Quellbild verknüpft sind.</p>
   <p>Auf 1 gesetzt, um basierend auf Alphakanaldaten zu beschneiden; Ecke wird ignoriert und 0 ist immer der Seed-Wert. Wenn dem Quellbild keine Alphakanaldaten zugeordnet sind, wird kein Zuschnitt angewendet.</p> 
   <p><i><b>Toleranz</b></i> - Toleranz. Real value 0.0 to 1.0. Gibt die Toleranz für übereinstimmende Pixelkomponentenwerte an. Für genaue Übereinstimmungen auf 0 setzen.</p>
   <p><i><b>infoFile</b></i> - Pfad und Name der XML-Ausgabedatei, in die die Zuschnittinformationen geschrieben werden.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Kopieren XMP Metadaten, falls verfügbar, aus <span class="codeph"> <span class="varname"> sourceFile </span> </span> nach <span class="codeph"> <span class="varname"> destFile </span> </span> ohne Änderung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Einbetten des ICC-Farbprofils in <span class="codeph"> <span class="varname"> destFile </span> </span>, sofern verfügbar (standardmäßig ist kein Profil eingebettet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name einer ICC-Profildatei. Definiert den Farbraum von <span class="codeph"> <span class="varname"> sourceFile </span> </span> und muss mit dem Pixeltyp übereinstimmen. Sollte nur angegeben werden, wenn kein Profil in <span class="codeph"> <span class="varname"> sourceFile </span> </span>, da dies das eingebettete Profil überschreibt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name einer ICC-Profildatei. Definiert den Pixeltyp und den Farbraum von <span class="codeph"> <span class="varname"> destFile </span> </span>. IC konvertiert in dieses Profil, wenn <span class="codeph"> <span class="varname"> sourceFile </span> </span> über ein eingebettetes Profil verfügt oder wenn <span class="codeph"> -imageprofile </span> wird ebenfalls angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Wahrnehmungsfähige Renderpriorität für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Relative farbmetrische Renderpriorität für Farbraumkonvertierungen (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Absolute farbmetrische Renderpriorität für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSamation </span> </p> </td> 
   <td colname="col2"> <p>Renderpriorität der Sättigung für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren der Blackpoint-Kompensation für bestimmte Farbkonvertierungen </p> <p>Standardmäßig aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie beim Farbkonvertieren das Dithering (Fehlerdiffusion). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -mainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Deaktivieren Sie die automatische Konvertierung von CMYK zu RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Erzwingen Sie die Dekodierung und Neukodierung von JPEG-Eingabebildern. </p> <p> <b>Vorsicht:</b> Die Anwendung dieser Option kann die Bildqualität beeinträchtigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen standardmäßigen (bilinearen) Resampling-Filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Filter mit höherer Qualität (Lanczos-Fenster) für die Neuberechnung (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Filter für die Neuberechnung mit höherer Qualität (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Neuberechnen mit dem Bikubisch-scharfen Photoshop-Filter 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Wenn als erste Option angegeben, unterdrückt die Ausgabe von Nutzungsinformationen, wenn ungültige Optionen gefunden werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -überschreiben </span> </p> </td> 
   <td colname="col2"> <p>Überschreiben einer vorhandenen <span class="codeph"> <span class="varname"> destFile </span> </span>. Standardmäßig wird ein numerisches Suffix an den Dateinamen angehängt, um ein Überschreiben zu verhindern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ignorieren Sie ausgeblendete Quelldateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>Beenden Sie die Verarbeitung nicht, wenn ein Fehler auftritt. Hat nur eine Auswirkung bei der Verarbeitung mehrerer Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name der Protokolldatei (standardmäßig <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Protokollebene. </p> 
   <p>&lt; 0 - Protokollierung deaktiviert.</p>
   <p>0 - Liste der zu verarbeitenden Dateien.</p>
   <p>1 - Hinzufügen von Berichten für nicht benötigte Dateien.</p>
   <p>2 - Fortschrittsberichte hinzufügen.</p>
   <p>3 - Fügen Sie Berichte zu jeder gefundenen Datei hinzu.</p>
   <p>4 - Fügen Sie Fortschrittsberichte auf Dateiebene hinzu.</p>
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
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Protokollierungsintervall in msec für Protokollebene 2 und höher (Standardwert ist 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> Bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Speicherauslastung. Muss mindestens 10 MB betragen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> Prozent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Speicherauslastung. Der Standardwert beträgt 25 % des physischen Speichers. Wenn <span class="codeph"> maxmem </span> nor <span class="codeph"> maxmempercent </span> explizit festgelegt werden, verwendet den maxmempercent-Standard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Version </span> </p> </td> 
   <td colname="col2"> <p> Gibt Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne weitere Optionen an. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Unterstützte Eingabebildformate {#section-ab13d941d6724e65b9f84b62d949d31c}

In der folgenden Tabelle sind die Bilddateiformate und Formatoptionen aufgeführt, die von IC unterstützt werden.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Pixeltyp</b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Komprimierung</b> </p> </th> 
   <th class="entry"> <p> <b> Anmerkungen</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows Bitmap) </p> </td> 
   <td> <p> RGB | indexiert </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> unkomprimiert | RLE </p> </td> 
   <td> <p> 5/6 Bit/Kanal zeigt Unterstützung für 16-Bit-RGB (5-5-5 und 5-6-5 Bit/Kanal) an. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated PostScript) </p> </td> 
   <td> <p> CMYK | RGB | grau </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | binär | JPEG </p> </td> 
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
   <td> <p> indexed </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
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
   <td> <p> CMYK | CMYKA | RGB | RGBA | grau | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> unkomprimiert | komprimiert </p> </td> 
   <td> <p> Nur zusammengeführtes Bild; Ebenen und zusätzliche Kanäle werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Nur Bitmap-Daten; Vektordaten werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | grau | grayA | indexiert </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> komprimiert </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grau | grayA | indexiert </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> unkomprimiert | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> Mit Ausnahme des ersten zugehörigen Alphakanals werden zusätzliche Kanäle ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

Eingebettete ICC-Profile werden in EPS-, JPG-, PSD-, PNG- und TIFF-Dateien erkannt.

Eingebettete Pfade und XMP Metadaten werden in EPS-, JPG-, PSD- und TIFF-Dateien erkannt.

## Beispiele {#section-3c1986b30315431989bd76b1ee5bef6d}

Konvertieren Sie ein einzelnes Bild in bestmöglicher Qualität und behalten Sie es im selben Ordner bei:

`ic -convert src/myFile.png src/myFile.tif`

Alle Bilder in konvertieren *`srcFolder`* JPEG-kodierte Pyramiden-TIFF und platzieren in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Alle Bilder in konvertieren *`srcFolder`*. Die kodierten Bilddaten von JPG-Dateien werden für die verlustfreie LZW-Komprimierung in voller Auflösung für die restliche Bildpyramide dieser-Bilder sowie für das gesamte Ausgabebild aller Nicht-JPG-Eingabedateien verwendet. Die Pixeltypen, eingebetteten Farbprofile, XMP Metadaten usw. verwaltet werden.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
