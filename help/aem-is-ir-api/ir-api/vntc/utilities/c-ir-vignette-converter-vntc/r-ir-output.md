---
description: vntc generiert Textdaten, die entweder an die Stderr- oder die Protokolldatei gesendet werden.
seo-description: vntc generiert Textdaten, die entweder an die Stderr- oder die Protokolldatei gesendet werden.
seo-title: Ausgabe
solution: Experience Manager
title: Ausgabe
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Output{#output}

vntc generiert Textdaten, die entweder an die Stderr- oder die Protokolldatei gesendet werden.

Die Daten werden als eine `name=value`-Eigenschaft pro Textdatensatz formatiert. Zeichenfolgenwerte werden nicht zitiert. Warn- und Fehlermeldungen werden immer an `stderr` gesendet, auch wenn `-log` angegeben ist.

Bestimmte Eigenschaften können mehrmals in derselben Ausgabe auftreten. An den Namen dieser Eigenschaften wird eine laufende Nummer angefügt, die mit 0 beginnt und durch einen Punkt getrennt wird. Solche Eigenschaften werden unten mit dem Suffix `. *`n`*` nach dem Eigenschaftsnamen gekennzeichnet.

Die folgenden Eigenschaften werden generiert:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Die RGB-Hintergrundfarbe des Möbelstils. Nur Möbelstile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Standardversion der Ausgabedatei. Auch die höchste Dateiversionsnummer, die in dieser Version von <span class="filepath"> vntc</span> generiert werden kann. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Fehler.<span class="varname"> n</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Fehlermeldung. Das Vorhandensein von Fehlermeldungen weist in der Regel darauf hin, dass entweder keine Ausgabedatei(n) erstellt wurde oder dass sie nicht für das Image Rendering geeignet sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Datei.<span class="varname"> n</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Der vollständig qualifizierte Pfad/Name aller Ausgabedateien, einschließlich Vignetten, Möbeldateien, Bilder mit voller Auflösung und Miniaturbilder. Für jede generierte Datei ist ein Dateiattribut vorhanden (mit Ausnahme der Protokolldatei). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1, wenn der Schrank Glastüren enthält, sonst 0. Nur Möbelstile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Der Name des in <span class="varname"> sourceFile</span> eingebetteten iccProfile. </p> <p>Leer, wenn <span class="varname"> sourceFile</span> nicht farbverwaltet wird. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Informationsbotschaft, z. B. Statusinformationen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1, wenn  <span class="varname"> </span> sourceFileis eine Übergeordnet Vignette ist, 0, wenn sie zuvor mit  <span class="filepath"> </span> vnUpdate oder  <span class="filepath"> vntc</span> verarbeitet wurde. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">übergeordnet=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> "</span> ivalis 0", wenn  <span class="varname"> </span> sourceFileis einen Schaltflächenstil enthält, der JPEG-Bilddaten enthält (in diesem Fall wird auch eine Warnung ausgegeben), andernfalls "1". Nur Möbel- und Fensterbehang für Stildateien. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Die maximale Speichergrenze, die für den laufenden <span class="filepath"> vntc</span>-Prozess gilt. <span class="varname"> Die </span> Zeichenfolge ist entweder  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> oder  <span class="codeph">  </span> 0(deaktiviert). wobei <span class="varname"> K</span>, <span class="varname"> M</span> und <span class="varname"> G</span> auf Kilobytes (1024 Byte), Megabytes (1048576 Byte) und Gigabytes (1073741824 verweisen ). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Skalierung der Pyramidenebene mit der niedrigsten Auflösung in der Vignette der Ausgabe. Nur vorhanden, wenn <span class="codeph"> -pyramid</span> angegeben ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Anzahl der in der <span class="varname"> sourceFile</span> gespeicherten Materialien. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Anzahl der Bereichsbilder in dieser Möbeldatei. Nur Möbelstile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Anzahl der Pyramidenebenen in der Vignette der Ausgabe. Nur vorhanden, wenn -pyramid angegeben ist. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0, wenn die Quell- oder Zielvignette eine Pyramidenstruktur aufweist. Nur Vignetten. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Bei Möbelstilen die Objektauflösung von sourceFile<span class="varname"> </span>. Bei Vignetten ist dies die empfohlene Materialauflösung für optimale Renderergebnisse bei der Wiedergabe der Ausgabe-Vignette. Pixel/Zoll (ppi). </p></td> 
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
  <td class="stentry"> <p>Der vollständig qualifizierte Pfad <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Dateiversion von <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Die Pixelgröße der Vignette für die Eingabe, das Standardbild für das Bedienfeld in einer Schrank-Datei oder das erste Deckkraftbild eines Fensters, das die Stildatei abdeckt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Die Art der Fensterbedeckung (nur für Fensterbedeckungsstile): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0 = horizontale Schattierung oder Jalousien </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1 = vertikale Jalousien </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2 = Kurze Vorhänge mit voller Breite </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3 = kurze Entwürfe links/rechts </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4 = Vorhänge mit voller Breite </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5 = linke/rechte, vollständige Drape </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=Café-Vorhang </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=Wert </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileis eine Vignette,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileis ein Schalterstil oder  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFileis ein Fensterbedeckungsstil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Der mit <span class="codeph"> -version</span> angegebene Wert oder der Wert von<span class="codeph"> defaultFileVersion</span>, wenn<span class="codeph"> -version</span> nicht angegeben wurde. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Kommagetrennte Liste der Pixelgrößen aller Ansichten in der Ausgabe-Vignette (die Ansicht mit voller Auflösung für Pyramidenvignetten), des Standardbildschirmbilds in einer Möbeldatei oder des ersten Deckkraftbilds einer Fensterbedeckungsdatei. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1, wenn der Möbelstil texturierbar ist, ansonsten 0. Nicht vorhanden für Vignetten- und Fensterverkleidungsstil-Dateien. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Warnung.<span class="varname"> n</span>=<span class="varname"> Zeichenfolge</span></span> </p></td> 
  <td class="stentry"> <p>Warnmeldung (z. B. wenn <span class="codeph"> -imagemap</span> angegeben ist, aber keine Kartendaten in der Vignette gefunden werden). </p></td> 
 </tr> 
</table>

