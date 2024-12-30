---
title: Allgemeine Optionen
description: Die folgenden Optionen können unabhängig vom Typ der Quelldatei angewendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Allgemeine Optionen{#common-options}

Die folgenden Optionen können unabhängig vom Typ der Quelldatei angewendet werden.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destPath <span class="varname"> Zeichenfolge </span> </span> </p> </td> 
  <td class="stentry"> <p>Ordner, in dem die Ausgabedateien abgelegt werden sollen (einschließlich der Protokolldatei, wenn <span class="codeph"> -log-</span> angegeben ist). Dies kann ein absoluter Pfad oder ein relativer Pfad zum aktuellen Arbeitsverzeichnis sein. Die Ordnerhierarchie wird erstellt, wenn sie nicht vorhanden ist. Sie gilt jedoch nicht für die mit <span class="codeph"> -log-</span> angegebene Datei. Wenn nicht anders angegeben, werden die Ausgabedateien in den Ordner geschrieben, in dem sich die <span class="varname">-Quelldatei </span>. Wenn <span class="varname"> destFile-</span> angegeben wird, wird sie immer an diesen Speicherort geschrieben, und <span class="codeph"> -destpath-</span> gilt nur für die sekundären Ausgabedateien. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Falls angegeben, wird das (erste) Ansichtsbild aus der Vignette, ein geeignetes Bereichsbild aus einem Schrankstil oder das erste Beleuchtungsbild eines Fensterabdeckungsstils extrahiert. Das extrahierte Bild wird als TIFF-Datei mit voller Auflösung gespeichert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Verhindert die Erstellung von Zieldateien. Hilfreich zum schnellen Extrahieren von Attributen aus einer <span class="varname">-</span>. Es werden nur die optionalen Miniaturansichten ( <span class="codeph"> -thumbwidth </span>), Bilder ( <span class="codeph"> -image </span>) und Protokolldateien ( <span class="codeph"> -log </span>) generiert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> Konkurrenzprodukt </span> </span> </p> </td> 
  <td class="stentry"> <p>Wählt verlustbehaftete JPEG-Kodierung für RGB- und Graustufen-Bilddaten, die in die Ausgabedatei eingebettet sind, anstelle von verlustfreiem PNG. Bilder mit Alpha (RGBA) werden immer mit PNG-Kodierung gespeichert. <span class="varname"> ival </span> gibt die JPEG-Qualität an (1…100); empfohlen wird eine Qualität von mindestens 85. Der Standardwert ist <span class="codeph"> -jpegquality 0 </span>, die die PNG-Codierung auswählt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> Pfad </span> </span> </p> </td> 
  <td class="stentry"> <p>Erstellt eine Protokolldatei mit dem angegebenen Pfad/Namen. Die vollständigen Pfade aller in den Zielordner geschriebenen Ausgabedateien werden in die Protokolldatei geschrieben. Außerdem werden einige zusätzliche Einstellungen wie Versionsinformationen und etwaige Warnungen oder Fehler in diese Datei geschrieben (Einzelheiten finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local">-</a>). Wenn <span class="codeph"> -log-</span> nicht angegeben ist, wird keine Protokolldatei erstellt. In diesem Fall wird die gesamte Textausgabe in <span class="codeph"> stdout-</span> geschrieben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerPriority <span class="varname"> Konkurrenzprodukt </span> </span> </p> </td> 
  <td class="stentry"> <p>Senken Sie die Priorität des <span class="filepath"> vntc-</span>. Dieser Prozess kann so verwendet werden, dass <span class="filepath"> VNTC-</span> bei der Verarbeitung einer Vignette nicht einen ganzen CPU übernimmt. Dadurch kann das Betriebssystem anderen, wichtigeren Prozessen mehr Zeit einräumen. <span class="varname"> ival </span> gibt den Prozentsatz der niedrigeren Priorität an (0..100). Der Standardwert ist <span class="codeph"> -lowerPriority 0 </span>, was die Priorität des <span class="filepath"> vntc-</span> nicht herabsetzt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Geben Sie die maximale Speicherkapazität an, die <span class="filepath"> vntc-</span> in Byte verwenden darf. Wenn <span class="filepath"> vntc-</span> die maximale Speicherbegrenzung erreicht, wird die Verarbeitung angehalten und ein Fehler ausgegeben. Der <span class="varname"> ival </span> gibt die maximale Speicherbegrenzung in Byte an (0.. 3 758 096 384 (3,5 GB)). Wenn <span class="varname"> ivale </span> 0 ist, wird die maximale Speicherbegrenzung deaktiviert. Der Standardwert ist <span class="codeph"> -maxmem 3221225472 </span>, was eine maximale Speicherbegrenzung von 3 GB bedeutet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "<span class="varname"> String </span>" </span> </p> </td> 
  <td class="stentry"> <p>Gibt das Trennzeichen zwischen dem Dateinamen und dem Suffix für Größe/Auflösung für automatisch generierte Ausgabedateinamen an. Die Standardeinstellung ist "-", wenn nicht anders angegeben. Ignoriert, wenn <span class="varname"> destFile-</span> oder <span class="codeph"> -info-</span> angegeben ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Schärfen <span class="varname"> rivalen </span> </span> </p> </td> 
  <td class="stentry"> <p>Ermöglicht das Scharfzeichnen von Bildern, die während der Verarbeitung neu gesampelt (skaliert) wurden. Gilt nur für das Scharfzeichnen von Miniaturansichten in kabinettartigen Dateien. </p> <p>Geben Sie 0 an, um das Scharfzeichnen zu deaktivieren (Standard), 1, um das normale Scharfzeichnen zu aktivieren, 2, um die Unschärfemaske nur für die Helligkeit zu aktivieren, oder 3, um die Unschärfemaske für jede Farbkomponente zu aktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -traceLevel </span> </p> </td> 
  <td class="stentry"> <p>Einstellung der Protokollebene Der Standardwert ist 1, wodurch alle Informations-, Warn- und Fehlermeldungen ausgegeben werden. Auf 0 gesetzt, um alle Meldungen außer Fehlermeldungen zu deaktivieren. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> Betrag </span> <span class="varname"> Radius </span> <span class="varname"> Schwellenwert </span> </span> </p> </td> 
  <td class="stentry"> <p>Legt die Unschärfemasken fest. Dieser Parameter wird ignoriert, wenn <span class="codeph"> -Sharpen-</span> auf 0 oder 1 gesetzt ist. Erforderlich, wenn <span class="codeph"> -Sharpen-</span> auf 2 oder 3 gesetzt ist. Der <span class="varname"> Betrag </span> ist ein reeller Wert im Bereich 0.0…500.0, der <span class="varname"> Radius </span> ein reeller Wert im Bereich 0.0…10.0 und der <span class="varname"> Schwellenwert </span> eine ganze Zahl von 0 bis 255. Weitere Informationen finden Sie in der Beschreibung von <span class="codeph"> op_usm= </span> in der Referenz zum Image-Serving-Protokoll . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateProduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Überprüfen Sie, ob die angegebene Vignette eine korrekte Produktionsvignette ist. Der <span class="varname"> ival </span> stellt die minimale Dateiversion der Vignette dar. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> Konkurrenzversion </span> </span> </p> </td> 
  <td class="stentry"> <p>Dateiversion für die Ausgabedatei. Wenn angegeben, muss es 0 oder eine gültige Vignettendateiversion sein (nicht größer als die standardmäßige Dateiversion). Wenn auf 0 oder nicht festgelegt, wird die Ausgabedatei mit der aktuellen Dateiversion erstellt. Dieser wird ignoriert, wenn <span class="codeph"> -info-</span> angegeben ist. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versionInfo </span> </p> </td> 
  <td class="stentry"> <p>Gibt Versionsinformationen für dieses Dienstprogramm aus. Geben Sie ohne Dateinamen und andere Optionen an. </p> </td> 
 </tr> 
</table>
