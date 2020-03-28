---
description: Die folgenden Optionen können unabhängig vom Typ sourceFile angewendet werden.
seo-description: Die folgenden Optionen können unabhängig vom Typ sourceFile angewendet werden.
seo-title: Allgemeine Optionen
solution: Experience Manager
title: Allgemeine Optionen
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Allgemeine Optionen{#common-options}

Die folgenden Optionen können unabhängig vom Typ sourceFile angewendet werden.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span></span> </p> </td> 
  <td class="stentry"> <p>Ordner, in dem die Ausgabedateien abgelegt werden sollen (einschließlich der Protokolldatei, falls <span class="codeph"> -log angegeben </span> ist). Kann ein absoluter Pfad oder relativ zum aktuellen Arbeitsverzeichnis sein. Die Ordnerhierarchie wird erstellt, wenn sie nicht vorhanden ist. Gilt nicht für die mit <span class="codeph"> -log angegebene Datei </span>. Falls nicht angegeben, werden die Ausgabedateien in den Ordner geschrieben, in dem sich die <span class="varname"> Quelldatei </span> befindet. Wenn die <span class="varname"> älteste Datei angegeben </span> ist, wird sie immer an diesen Speicherort geschrieben, und <span class="codeph"> -destpath gilt </span> nur für die sekundären Ausgabedateien. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Bild </span> </p> </td> 
  <td class="stentry"> <p>Falls angegeben, wird das Bild der (ersten) Ansicht aus der Vignette, einem geeigneten Bereichsbild aus einem Schrankstil oder dem ersten Beleuchtungsbild eines Fensterbedeckungsstils extrahiert. Das extrahierte Bild wird als TIFF-Datei mit voller Auflösung gespeichert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Verhindert die Erstellung von Zielgruppen-Dateien. Nützlich zum schnellen Extrahieren von Attributen aus der <span class="varname"> Quelldatei </span>. Es werden nur die optionalen Miniaturansichten ( <span class="codeph"> -thumbwidth </span>), das Bild ( <span class="codeph"> -image </span>) und die Protokolldateien ( <span class="codeph"> -log </span>) generiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Wählt verlustbehaftete JPEG-Kodierung für in die Ausgabedatei eingebettete RGB- und Graustufenbilddaten statt verlustfreier PNG-Datei aus. Bilder mit Alpha (RGBA) werden immer mit PNG-Kodierung gespeichert. <span class="varname"> ival </span> gibt die JPEG-Qualität (1...100) an. 85 oder höher wird empfohlen. Der Standardwert ist <span class="codeph"> -jpegquality 0 </span>, wodurch die PNG-Kodierung ausgewählt wird. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span></span> </p> </td> 
  <td class="stentry"> <p>Erstellt eine Protokolldatei mit dem angegebenen Pfad/Namen. Die vollständigen Pfade aller in den Zielordner geschriebenen Ausgabedateien werden in die Protokolldatei geschrieben. Außerdem werden einige zusätzliche Einstellungen wie Versionsinformationen und ggf. auftretende Warnungen oder Fehler angezeigt (weitere Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Ausgabe </a> ). Es wird keine Protokolldatei erstellt, wenn <span class="codeph"> -log nicht angegeben </span> ist. in diesem Fall wird die gesamte Textausgabe in <span class="codeph"> stdout geschrieben </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> Inaktiv mit niedrigerer Priorität </span></span> </p> </td> 
  <td class="stentry"> <p>Verringern Sie die Priorität des <span class="filepath"> vntc- </span> Prozesses. Dies kann verwendet werden, damit <span class="filepath"> vntc während der Verarbeitung einer Vignette </span> nicht die gesamte CPU übernimmt. Es ermöglicht dem Betriebssystem, anderen, wichtigeren Prozessen mehr Zeit zu geben. <span class="varname"> ival </span> gibt den Prozentsatz der niedrigeren Priorität (0..100) an. Die Standardeinstellung ist <span class="codeph"> -low priority 0 </span>, was die Priorität des <span class="filepath"> vntc- </span> Prozesses nicht verringert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Geben Sie die maximale Speicherkapazität an, die <span class="filepath"> vntc in Byte verwenden </span> darf. Wenn <span class="filepath"> vntc die maximale Speichergrenze </span> erreicht, wird die Verarbeitung beendet und es wird ein Fehler ausgegeben. <span class="varname"> ival </span> gibt die maximale Speichergrenze in Byte (0) an. 3.758.096.384 (3,5 GB). Wenn <span class="varname"> ival 0 </span> ist, wird die maximale Speichergrenze deaktiviert. Der Standardwert ist <span class="codeph"> -maxmem 3221225472 </span>, d. h. eine maximale Speichergrenze von 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Gibt das Trennzeichen zwischen dem Dateinamen und dem Suffix für Größe/Auflösung für automatisch generierte Ausgabedateinamen an. Die Standardeinstellung ist "-", wenn nicht angegeben. Wird ignoriert, wenn <span class="varname"> destFile </span> oder <span class="codeph"> -info </span> angegeben ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Aktiviert das Scharfzeichnen von Bildern, die während der Verarbeitung neu berechnet (skaliert) wurden. Gilt nur für das Scharfzeichnen von Miniaturbildern bei Dateien im Schrank-Stil. </p> <p>Geben Sie 0 an, um die Scharfzeichnung zu deaktivieren (Standard), 1, um die normale Scharfzeichnung zu aktivieren, 2, um die Unschärfemaske nur für die Helligkeit zu aktivieren, oder 3, um die Unschärfemaske für jede Farbkomponente zu aktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Zugreifen </span> </p> </td> 
  <td class="stentry"> <p>Legt die Protokollierungsstufe fest. Der Standardwert ist 1, der alle Informations-, Warn- und Fehlermeldungen ausgibt. Auf 0 setzen, um alle Meldungen außer Fehlermeldungen zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> Betrag </span><span class="varname"> Radius </span><span class="varname"> Schwellenwert </span></span> </p> </td> 
  <td class="stentry"> <p>Legt die Parameter für die Unschärfemaske fest. Ignoriert, wenn <span class="codeph"> -sharpen auf 0 oder 1 eingestellt </span> ist; erforderlich, wenn <span class="codeph"> -sharpen auf 2 oder 3 eingestellt </span> ist. <span class="varname"> Betrag </span> ist ein echter Wert im Bereich 0.0...500.0, <span class="varname"> Radius </span> ist ein echter Wert im Bereich 0.0...10.0 und <span class="varname"> Schwellenwert </span> ist eine Ganzzahl zwischen 0 und 255. Weitere Informationen finden Sie in der Beschreibung zu <span class="codeph"> op_usm= </span> in der Image Serving Protocol Reference. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Überprüfen Sie, ob es sich bei der angegebenen Vignette um eine ordnungsgemäße Vignette für die Produktion handelt. <span class="varname"> ival </span> stellt die minimale Dateiversion der Vignette dar. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Dateiversion für die Ausgabedatei. Wenn angegeben, muss die Vignettendateiversion 0 oder eine gültige Version sein (nicht größer als die Standarddateiversion). Wenn der Wert auf 0 festgelegt ist oder nicht, wird die Ausgabedatei mit der aktuellsten Dateiversion erstellt. Wird ignoriert, wenn <span class="codeph"> -info </span> angegeben ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Gibt Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne Dateinamen und andere Optionen an. </p> </td> 
 </tr> 
</table>

