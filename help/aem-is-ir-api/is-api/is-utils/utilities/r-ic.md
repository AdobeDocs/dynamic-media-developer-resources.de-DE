---
description: Bildkonvertierungsdienstprogramm.
seo-description: Bildkonvertierungsdienstprogramm.
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9

---


# ic {#ic}

Bildkonvertierungsdienstprogramm.

`ic` ist ein Befehlszeilenwerkzeug, das Bilddateien in das optimierte Pyramid TIFF-Format (PTIFF) konvertiert. Beim Image Serving können Bilder ohne Konvertierung verarbeitet werden. Es wird jedoch empfohlen, alle Bilder, die größer als 512 x 512 Pixel sind, in das PTIFF-Format zu konvertieren. Diese Konvertierung gewährleistet eine optimale Serverleistung und Ressourcennutzung und minimiert die Reaktionszeiten.

Es wird empfohlen, dass PTIFF-Dateien, die fotografischen Inhalt enthalten, JPEG-kodiert werden (geben Sie `-jpegcompress`an). Computer-generierte Inhalte können verlustfrei komprimiert werden (entweder `-deflatecompress` oder `-lzwcompress`). Sofern keine Farbkonvertierung oder Pixeltypkonvertierung erforderlich ist, werden die JPEG-Quellbilddaten ohne Dekodierung in das PTIFF übertragen, um eine Qualitätsminderung zu vermeiden. In diesem Fall gelten die angegebenen Komprimierungsoptionen nur für die Pyramidenebenen mit niedrigerer Auflösung.

Wenn Sie keine großen Bilder konvertieren, müssen Sie nicht die Parameter einstellen, die steuern, wie viel Arbeitsspeicher Sie verwenden. Wenn Sie dies tun, geben Sie jedoch `ic` mehr Speicher, indem Sie die unten beschriebene `-maxmem` Einstellung verwenden. Eine gute Faustregel für die Berechnung der erforderlichen Speichermenge ist die Multiplikation der Bildbreite mit der Bildhöhe und der Anzahl der Kanal. Beispiel: Vier für ein RGB-Bild mit dem Alphabet mal drei. Wenn die Kanal 16 Bit pro Komponente anstelle von 8 Dubletten betragen, ergibt sich das Endergebnis.

## Nutzung {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>Optionen</i> </span></span> </p> </td> 
   <td colname="col2"> <p>Befehlsoptionen (siehe unten). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sourceFile <i></i> </span></span> </p> </td> 
   <td colname="col2"> <p>Einzelne Eingabebilddatei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span></span> </p> </td> 
   <td colname="col2"> <p>PTIFF-Ausgabedatei (bei Verwendung mit SourceDirectory nicht gültig). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>Ordner mit Eingabebildern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>Ordner, in den die PTIFF-Ausgabedateien geschrieben werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-36a2dcfa39824d29b69547c432366219}

0, wenn erfolgreich. Wenn ein Fehler auftritt, wird ein Wert ungleich null zurückgegeben und Fehlerdetails werden an gesendet `stderr`.

## Optionen {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nicht komprimiert </span> </p> </td> 
   <td colname="col2"> <p>Komprimieren Sie das Ausgabebild nicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Deflate-Komprimierung (zip) (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die Komprimierung Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie die JPEG-Kodierung. Wird ignoriert, wenn <span class="codeph"> die <span class="varname"> Quelldatei </span> </span> Alpha-Daten enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG-Qualität (0-100; default ist 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominanz </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie das JPEG-Chrominanzierungsschema (kann die Qualität von Farbtext und Grafiken verbessern). Dies hat keine Auswirkungen auf Ausgabebilder, die CMYK oder Graustufen sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> Betrag </span>&gt; &lt; <span class="varname"> Radius </span>&gt; &lt; <span class="varname"> Schwellenwert </span>&gt; &lt; <span class="varname"> Monochrom </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Wenden Sie die Unschärfemaske auf die Pyramidenebenen an. Weitere Informationen finden Sie unter <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> . (Nicht auf das Bild mit voller Auflösung angewendet.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie ggf. den Clip-Pfad in der Quelldatei, um die zugehörigen Alpha-Daten zu erstellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Druckauflösung (dpi) für die <span class="codeph"> älteste <span class="varname"> Datei </span> </span>; Wenn nicht angegeben, wird die Druckauflösung von <span class="codeph"> srcFile </span> in die <span class="codeph"> ältesteDatei kopiert <span class="varname"> </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocut &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> oleranz </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Berechnen Sie ein Rechteck für das Beschneiden, um den Hintergrund für die Volltonfarbe zu minimieren. Es werden keine Informationen zum Beschneiden ausgegeben, wenn der Algorithmus zum automatischen Beschneiden dazu führen würde, dass das gesamte Bild beschnitten wird. </p> <p>Um das Rechteck für die Beschneidung ohne Konvertierung des Bilds zu berechnen, geben Sie <span class="codeph"> - autocut </span> ohne <span class="codeph"> -convert </span> und ohne <span class="codeph"> <span class="varname"> destFile an.</span> </span></p>

<p><i><b>corner</b></i> - ul| EUR| ll| lr </p>
   <p> Gibt an, welche Bildecke ein Seed-Point verwendet werden soll. Wird ignoriert, wenn der Modus 1 ist.</p>
   <p><i><b>mode</b></i> - 0| 1</p>
   <p>auf 0 setzen, um je nach Farbe des angegebenen Eckpixel abgeschnitten zu werden; funktioniert mit vormultiplizierten Farbdaten, wenn Alpha-Daten mit dem Quellbild verknüpft sind.</p>
   <p>Auf 1 setzen, um basierend auf Alpha-Daten zu beschneiden; corner wird ignoriert und 0 ist immer der Seed-Wert. Es wird keine Beschneidung angewendet, wenn keine Alpha-Daten mit dem Quellbild verknüpft sind.</p> 
   <p><i><b>Toleranz</b></i> - Übereinstimmung mit Toleranz Real value 0.0 to 1.0. Gibt die Toleranz für übereinstimmende Pixelkomponentenwerte an. Für genaue Übereinstimmungen auf 0 setzen.</p>
   <p><i><b>infoFile</b></i> - Pfad und Name der XML-Ausgabedatei, in die die Daten zum Beschneiden geschrieben werden.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Kopieren Sie, falls verfügbar, XMP-Metadaten aus der <span class="codeph"> Quelldatei <span class="varname"> in die </span> ältesteDatei </span> , <span class="codeph"> <span class="varname"> </span> </span> ohne Änderungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Einbetten des ICC-Profils in die <span class="codeph"> älteste <span class="varname"> Datei </span> </span>(falls verfügbar) (standardmäßig ist kein Profil eingebettet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name einer ICC-Profil-Datei. Definiert den Farbraum der <span class="codeph"> Quelldatei <span class="varname"> </span> </span> und muss mit dem Pixeltyp übereinstimmen. Sollte nur angegeben werden, wenn kein Profil in die <span class="codeph"> Quelldatei eingebettet ist <span class="varname"></span> </span>, da dies das eingebettete Profil überschreibt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pfad und Name einer ICC-Profil-Datei. Definiert den Pixeltyp und den Farbraum der <span class="codeph"> ältesten <span class="varname"> Datei </span> </span>. IC konvertiert in dieses Profil, wenn die <span class="codeph"> Quelldatei ein eingebettetes Profil <span class="varname"> hat oder wenn </span> -imageprofile ebenfalls angegeben </span> <span class="codeph"> </span> ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Perzeptive Renderpriorität für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Relative kolorimetrische Renderpriorität für Farbraumkonvertierungen (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Absolute farbmetrische Renderpriorität für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Renderpriorität der Sättigung für Farbraumkonvertierungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren der Blackpoint-Kompensation für bestimmte Farbkonvertierungen </p> <p>Standardmäßig aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Deaktivieren Sie Dithering (Fehlerdiffusion) bei der Farbkonvertierung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -betreuainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Deaktivieren Sie die automatische Konvertierung von CMYK in RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Erzwingen Sie die Dekodierung und Neukodierung von JPEG-Eingabebildern. </p> <p> <b>Vorsicht:</b> Durch Anwendung dieser Option kann die Bildqualität beeinträchtigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Filter für die Standardqualität (bi-linear). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Filter für eine höhere Qualität (Lanczos-Fenster) zum Neuberechnen (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Verwenden Sie einen Filter für eine höhere Qualität (FlashPix) zum Neuberechnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Neuberechnen mit Fotoshop-Stil 8 x 8 bikubisch scharf Filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Unterdrückt, wenn als erste Option angegeben, die Ausgabe von Nutzungsinformationen, wenn ungültige Optionen gefunden werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -überschreiben </span> </p> </td> 
   <td colname="col2"> <p>Überschreiben einer vorhandenen <span class="codeph"> ältesten <span class="varname"> Datei zulassen </span></span>. Standardmäßig wird ein numerisches Suffix an den Dateinamen angehängt, um ein Überschreiben zu verhindern. </p> </td> 
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
   <td colname="col2"> <p>Pfad und Name der Protokolldatei (standardmäßig " <span class="codeph"> stdout" </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Protokollierungsstufe </p> 
   <p>&lt; 0 - Protokollierung deaktiviert.</p>
   <p>0 - zu verarbeitende Listen.</p>
   <p>1 - Hinzufügen Berichte für nicht benötigte Dateien.</p>
   <p>2 - Hinzufügen Berichte.</p>
   <p>3 - Hinzufügen Berichte auf jeder Datei gefunden.</p>
   <p>4 - Hinzufügen Berichte zum Fortschritt auf Dateiebene.</p>
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
   <td colname="col2"> <p>Protokollierungsintervall in msec für Loglevel 2 und höher (Standard ist 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Speicherbelegungsgrenze. Muss mindestens 10 MB betragen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Speicherbelegungsgrenze. Der Standardwert beträgt 25 % des physischen Speichers. Wenn weder <span class="codeph"> maxmem </span> noch <span class="codeph"> maxmempercent explizit festgelegt </span> sind, verwendet maxmempercent default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Version </span> </p> </td> 
   <td colname="col2"> <p> Gibt Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne weitere Optionen an. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Unterstützte Eingabebildformate {#section-ab13d941d6724e65b9f84b62d949d31c}

In der folgenden Tabelle werden die Bilddateiformate und Formatoptionen Liste, die von IC unterstützt werden.

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
   <td> <p> RGB| indexiert </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> unkomprimiert| RLE </p> </td> 
   <td> <p> 5/6 Bit/Kanal deutet auf eine Unterstützung für 16-Bit-RGB (5-5-5 und 5-6-5 Bit/Kanal) hin. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated PostScript) </p> </td> 
   <td> <p> CMYK| RGB| grau </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII| ASCII85| Binär| JPEG </p> </td> 
   <td> <p> Nur von Fotoshop generierte EPS-Dateien werden unterstützt. </p> </td> 
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
   <td> <p> indexiert </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> Ist dies der Fall, wird der Transparenzwert in der Palette in Alpha umgewandelt. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK| RGB| grau </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA| grau| grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> unkomprimiert| komprimiert </p> </td> 
   <td> <p> Nur zusammengeführtes Bild; Ebenen und zusätzliche Kanal werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Nur Bitmapdaten; Vektordaten werden ignoriert. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB| RGBA| grau| grayA| indexiert </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> komprimiert </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA| grau| grayA| indexiert </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> unkomprimiert| ZIP| LZW| JPEG| CCITT RLE| CCITT G3| CCITT G4| Pakete </p> </td> 
   <td> <p> Mit Ausnahme des ersten verknüpften Alpha-Kanals werden zusätzliche Kanal ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

Eingebettete ICC-Profil werden in den Dateien EPS, JPG, PSD, PNG und TIFF erkannt.

Eingebettete Pfade und XMP-Metadaten werden in EPS-, JPG-, PSD- und TIFF-Dateien erkannt.

## Beispiele {#section-3c1986b30315431989bd76b1ee5bef6d}

Konvertieren Sie ein einzelnes Bild in bester Qualität und behalten Sie es im selben Ordner bei:

`ic -convert src/myFile.png src/myFile.tif`

Konvertieren Sie alle Bilder in *`srcFolder`* JPEG-kodierte Pyramide-TIFFs und platzieren Sie sie in *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Konvertieren Sie alle Bilder in *`srcFolder`*. Die kodierten Bilddaten von JPG-Dateien werden für die verlustfreie LZW-Komprimierung mit voller Auflösung für den Rest der Bildpyramide dieser Bilder sowie für das gesamte Ausgabebild aller Nicht-JPG-Eingabedateien verwendet. Die Pixeltypen, eingebetteten Profile, XMP-Metadaten usw. werden beibehalten.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
