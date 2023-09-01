---
title: Allgemeine Optionen
description: Die folgenden Optionen können unabhängig vom Typ der sourceFile angewendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# Allgemeine Optionen{#common-options}

Die folgenden Optionen können unabhängig vom Typ der sourceFile angewendet werden.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> Zeichenfolge </span> </span> </p> </td> 
  <td class="stentry"> <p>Ordner, in dem die Ausgabedateien abgelegt werden sollen (einschließlich der Protokolldatei, falls <span class="codeph"> -log </span> angegeben ist). Dies kann ein absoluter Pfad oder ein relativer Pfad zum aktuellen Arbeitsverzeichnis sein. Die Ordnerhierarchie wird erstellt, wenn sie nicht vorhanden ist. Sie gilt jedoch nicht für die mit <span class="codeph"> -log </span>. Falls nicht angegeben, werden die Ausgabedateien in den Ordner geschrieben, in dem die <span class="varname"> sourceFile </span> befindet. Wenn <span class="varname"> destFile </span> festgelegt ist, wird er immer an diesen Speicherort geschrieben und <span class="codeph"> -destpath </span> gilt nur für die sekundären Ausgabedateien. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Bild </span> </p> </td> 
  <td class="stentry"> <p>Falls angegeben, wird das (erste) Ansichtsbild aus der Vignette, einem geeigneten Panelbild aus einem Schrank-Stil oder dem ersten Beleuchtungsbild eines Fensterbedeckungsstils extrahiert. Das extrahierte Bild wird als TIFF-Datei mit voller Auflösung gespeichert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Verhindert die Erstellung von Zieldateien. Nützlich zum schnellen Extrahieren von Attributen aus einer <span class="varname"> sourceFile </span>. Nur die optionale Miniaturansicht ( <span class="codeph"> -thumbwidth </span>), Bild ( <span class="codeph"> -image </span>) und Protokolldateien ( <span class="codeph"> -log </span>) generiert werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Wählt verlustbehaftete JPEG-Kodierung für RGB- und Graustufenbilddaten aus, die in die Ausgabedatei eingebettet sind, anstatt verlustfreies PNG. Bilder mit Alpha (RGBA) werden immer mit PNG-Kodierung gespeichert. <span class="varname"> ival </span> Angabe der JPEG-Qualität (1...100); empfohlen wird mindestens 85. Der Standardwert ist <span class="codeph"> -jpegquality 0 </span>, der die PNG-Kodierung auswählt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>Erstellt eine Protokolldatei mit dem angegebenen Pfad/Namen. Die vollständigen Pfade aller Ausgabedateien, die in den Zielordner geschrieben wurden, werden in die Protokolldatei geschrieben. Außerdem werden einige zusätzliche Einstellungen wie Versionsinformationen und etwaige Warnungen oder Fehler aufgeführt (siehe <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Ausgabe </a> für Details). Es wird keine Protokolldatei erstellt, wenn <span class="codeph"> -log </span> nicht angegeben ist; in diesem Fall wird die gesamte Textausgabe in <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Verringern Sie die Priorität der <span class="filepath"> vntc </span> -Prozess. Dieser Prozess kann verwendet werden, damit <span class="filepath"> vntc </span> übernimmt bei der Verarbeitung einer Vignette nicht die gesamte CPU. Dadurch kann das Betriebssystem anderen, wichtigeren Prozessen mehr Zeit geben. <span class="varname"> ival </span> gibt den Prozentsatz der niedrigeren Priorität an (0.100). Der Standardwert ist <span class="codeph"> -lowerpriority 0 </span>, wodurch die Priorität der <span class="filepath"> vntc </span> -Prozess. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Geben Sie die maximale Speicherkapazität an, die <span class="filepath"> vntc </span> darf in Byte verwendet werden. Wann <span class="filepath"> vntc </span> die maximale Speicherbegrenzung erreicht, stoppt die Verarbeitung und erzeugt einen Fehler. Die <span class="varname"> ival </span> gibt die maximale Speicherbegrenzung in Byte (0) an. 3.758.096.384 (3,5 GB). Wann <span class="varname"> ival </span> auf 0 gesetzt ist, ist die maximale Speicherbegrenzung deaktiviert. Der Standardwert ist <span class="codeph"> -maxmem 3221225472 </span>, was eine maximale Speicherbegrenzung von 3 GB bedeutet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> Zeichenfolge </span>" </span> </p> </td> 
  <td class="stentry"> <p>Gibt das Trennzeichen zwischen dem Dateinamen und dem Suffix für die Größe/Auflösung für automatisch generierte Ausgabedateinamen an. Die Standardeinstellung ist "-", falls nicht angegeben. Ignoriert , wenn <span class="varname"> destFile </span> oder <span class="codeph"> -info </span> festgelegt ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Aktiviert die Scharfzeichnung von Bildern, die während der Verarbeitung neu berechnet (skaliert) werden. Gilt nur für das Scharfzeichnen von Miniaturansichten in Dateien im Schrank-Stil. </p> <p>Geben Sie 0 zum Deaktivieren der Scharfzeichnung (Standard), 1 zum Aktivieren der normalen Scharfzeichnung, 2 zum Aktivieren der Unschärfemaske nur für die Helligkeit oder 3 zum Aktivieren der Unschärfemaske für jede Farbkomponente an. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Trittbrett </span> </p> </td> 
  <td class="stentry"> <p>Legt die Protokollebene fest. Der Standardwert ist 1, der alle Informations-, Warn- und Fehlermeldungen ausgibt. Auf 0 setzen, um alle außer Fehlermeldungen zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> amount </span> <span class="varname"> radius </span> <span class="varname"> Schwellenwert </span> </span> </p> </td> 
  <td class="stentry"> <p>Legt die Parameter für die Unschärfemaske fest. Ignoriert , wenn <span class="codeph"> -sharpen </span> auf 0 oder 1 festgelegt ist, erforderlich, wenn <span class="codeph"> -sharpen </span> auf 2 oder 3 festgelegt ist. Die <span class="varname"> amount </span> einen realen Wert im Bereich 0.0...500.0 hat, wird die <span class="varname"> radius </span> ist ein echter Wert im Bereich 0.0...10.0 und die Variable <span class="varname"> Schwellenwert </span> ist eine Ganzzahl von 0 bis 255. Siehe Beschreibung von <span class="codeph"> op_usm= </span> in der Image Serving Protocol-Referenz für weitere Informationen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Überprüfen Sie, ob es sich bei der angegebenen Vignette um eine ordnungsgemäße Produktionsvignette handelt. Die <span class="varname"> ival </span> stellt die minimale Dateiversion der Vignette dar. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Dateiversion für die Ausgabedatei. Wenn angegeben, muss die Vignettendatei 0 oder eine gültige Vignettendateiversion sein (nicht größer als die Standarddateiversion). Wenn der Wert auf 0 gesetzt oder nicht angegeben ist, wird die Ausgabedatei mit der aktuellsten Dateiversion erstellt. Ignoriert , wenn <span class="codeph"> -info </span> festgelegt ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Gibt Versionsinformationen für dieses Dienstprogramm zurück. Geben Sie ohne Dateinamen und andere Optionen an. </p> </td> 
 </tr> 
</table>
