---
description: VNTC generiert Textdaten, die entweder an STDERR oder die Protokolldatei gesendet werden.
solution: Experience Manager
title: Ausgabe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Ausgabe{#output}

VNTC generiert Textdaten, die entweder an STDERR oder die Protokolldatei gesendet werden.

Die Daten werden als eine `name=value` pro Textdatensatz formatiert. Zeichenfolgenwerte werden nicht in Anführungszeichen gesetzt. Warn- und Fehlermeldungen werden immer an `stderr` gesendet, auch wenn `-log` angegeben ist.

Bestimmte Eigenschaften können in derselben Ausgabe mehrmals auftreten. An den Namen dieser Eigenschaften wird eine Sequenznummer angehängt, die mit 0 beginnt und durch einen Punkt getrennt ist. Solche Eigenschaften werden unten mit einem Suffix `. *`n`*` nach dem Eigenschaftsnamen gekennzeichnet.

Die folgenden Eigenschaften werden generiert:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">BGC=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Die RGB-Hintergrundfarbe des Schrankstils. Nur Schrankstile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Standardversion der Ausgabedatei. Auch die höchste Dateiversionsnummer, die diese Version <span class="filepath"> vntc</span> erzeugen kann. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Fehler.<span class="varname"> N</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Fehlermeldung. Fehlermeldungen weisen in der Regel darauf hin, dass entweder keine Ausgabedatei(en) erstellt wurden oder dass sie für die Verwendung durch das Bild-Rendering nicht geeignet sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Datei.<span class="varname"> N</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Der vollständig qualifizierte Pfad/Name aller Ausgabedateien, einschließlich Vignetten, Cabinet-Style-Dateien, Bildern mit voller Auflösung und Miniaturbildern. Für jede generierte Datei (mit Ausnahme der Protokolldatei) ist ein Dateiattribut vorhanden. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Glas=<span class="varname"> Rival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> ist 1, wenn der Schrank Glastüren enthält, andernfalls 0. Nur Schrankstile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> String</span></span> </p></td> 
  <td class="stentry"> <p>Der Name des in die <span class="varname">-Quelldatei eingebetteten iccProfile</span>. </p> <p>Leer, wenn <span class="varname"> Quelldatei </span> nicht farbverwaltet wird. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Info.<span class="varname"> N</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Informationsmeldung, z. B. Fortschrittsinformationen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> Rival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> ist 1, wenn <span class="varname"> sourceFile</span> eine Master-Vignette ist, 0, wenn sie zuvor mit <span class="filepath"> vnUpdate</span> oder <span class="filepath"> vntc</span> verarbeitet wurde. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> rival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> ist 0, wenn <span class="varname"> sourceFile</span> ein Schrankstil ist, der JPEG-Bilddaten enthält (in diesem Fall wird auch eine Warnung ausgegeben), andernfalls 1. Gehäuse und Fenster, die nur Stildateien abdecken. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> String</span></span> </p></td> 
  <td class="stentry"> <p>Die maximale Speicherbegrenzung, die für den laufenden <span class="filepath"> vntc</span>-Prozess gilt. <span class="varname"> Zeichenfolge </span> entweder <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span> oder <span class="codeph"> 0</span> (deaktiviert). Dabei beziehen sich <span class="varname"> K</span>, <span class="varname"> M</span> und <span class="varname"> G</span> auf Kilobyte (1024 Byte), Megabyte (1048576 Byte) und Gigabyte (1073741824 Byte). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> Rival</span></span> </p></td> 
  <td class="stentry"> <p>Skalierung des niedrigsten Auflösungspyramidenpegels in der Ausgangsvignette. Nur vorhanden, wenn <span class="codeph"> -Pyramide</span> angegeben ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Anzahl der in der <span class="varname">-Quelldatei gespeicherten </span>. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Anzahl der Bereichsbilder in dieser Kabinettstildatei. Nur Schrankstile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> rival</span></span> </p></td> 
  <td class="stentry"> <p>Die Anzahl der Pyramidenebenen in der Ausgabevignette. Nur vorhanden, wenn -pyramid angegeben ist. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Pyramid=<span class="varname"> Rival</span></span> </p></td> 
  <td class="stentry"> <p>0, wenn entweder die Quell- oder Zielvignette eine Pyramidenstruktur hat. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Für Kabinettstile die Objektauflösung der <span class="varname">sourceFile</span>. Für Vignetten ist dies die empfohlene Materialauflösung für die Renderergebnisse der besten Qualität beim Rendern der Ausgabevignette. Pixel/Zoll (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Die kleinste Objektauflösung in der Ausgabevignette. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Die durchschnittliche Objektauflösung in der Ausgabevignette. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Der vollständig qualifizierte <span class="varname"> sourceFile</span>Pfad. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Dateiversion <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Pixelgröße der Eingabevignette, das Standardbild des Bedienfelds in einer Kabinettstil-Datei oder das erste Deckkraftbild eines Fensters, das eine Stildatei abdeckt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Typ der Fensterabdeckung (nur Formatvorlagen für Fensterabdeckung): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=Horizontalschatten oder Jalousien </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=Vertikaljalousien </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=Kurze Vorhänge in voller Breite </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=Kurze Vorhänge links/rechts </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=Vorhänge in voller Breite </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=Vorhänge in voller Länge links/rechts </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=Café-Vorhang </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=Ausgewogenheit </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> String</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> Wenn <span class="varname"> sourceFile</span> eine Vignette ist, <span class="codeph"> vnc</span> wenn <span class="varname"> sourceFile</span> ein Schrankstil ist, oder <span class="codeph"> vnw</span> wenn <span class="varname"> sourceFile</span> ein Fensterabdeckungsstil ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Der mit <span class="codeph"> -version</span> angegebene Wert oder der Wert von <span class="codeph">defaultFileVersion</span>, wenn <span class="codeph"> -version</span> nicht angegeben wurde. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSize=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Durch Kommas getrennte Liste der Pixelgrößen aller Ansichten in der Ausgabevignette (die Ansicht mit voller Auflösung für Pyramidenvignetten), des Standardbedienfeldbilds in einer Kabinettstil-Datei oder des ersten Deckkraftbilds einer Fensterabdeckungs-Stildatei. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> ist 1, wenn der Schrankstil texturierbar ist, andernfalls 0. Nicht vorhanden für Vignetten und Fensterabdeckungen Style Files. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Warnung<span class="varname"> N</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Warnmeldung (z. B. wenn <span class="codeph"> -imagemap</span> angegeben wird, aber keine Kartendaten in der Vignette gefunden werden). </p></td> 
 </tr> 
</table>
