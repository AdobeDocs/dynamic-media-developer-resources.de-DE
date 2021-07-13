---
description: Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.
solution: Experience Manager
title: Optionen für Vignetten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Optionen für Vignetten{#options-for-vignettes}

Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -Inhalt</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine XML-Datei, die die Objekthierarchie einschließlich der ausgewählten Objektattribute darstellt. Der Inhalt der Datei entspricht dem vom Befehl <span class="codeph"> req=contents</span> zurückgegebenen Inhalt. Die Datei hat denselben Namen wie die Quelldatei, jedoch mit dem Suffix <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Zuschneiden der Vignette vor Skalierung. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> </span></span> ist die obere linke Ecke des Zuschnittrechtecks und  <span class="codeph"><span class="varname"> bred</span>, <span class="varname"> </span></span> ist die Größe des Zuschnittrechtecks. Die Werte sind Pixelkoordinaten, die relativ zum Vollbildansicht der Quellvignette sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Zuschneiden der Vignette vor Skalierung. </p> <p><span class="codeph"><span class="varname"> xn</span>, <span class="varname"> </span></span> ynis die obere linke Ecke des Zuschnittrechtecks und  <span class="codeph"><span class="varname"> bredn</span>,<span class="varname"> </span></span> entspricht der Größe des Zuschnittrechtecks. Die Werte werden relativ zum Ansichtsbild der Quellvignette normalisiert und müssen zwischen 0,0...1.0 liegen. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinmust be not greater than 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -einbettbare Materialien</span> </p></td> 
  <td class="stentry"> <p>Bewahren Sie eingebettete Materialien in der Vignette der Ausgabe auf. Standardmäßig werden Materialien aus der Vignette entfernt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabevignettenhöhen in Pixel. Wird ignoriert, wenn -info angegeben ist. <span class="varname"> </span> kann 0 betragen, was die Breite der Vignette angibt. Detaillierte Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Aktivieren Sie die Extraktion der Imagemap-Datei aus der Vignette. Die Zuordnungsdaten werden in eine HTML-Datei geschrieben, die nur ein <span class="codeph"> &lt;map&gt;</span> -Element enthält. Die Ausgabedatei hat denselben Namen wie die Ausgabebilddatei, allerdings mit dem Suffix <span class="filepath"> .htm</span>. Es wird eine Warnmeldung erzeugt und keine Datei erstellt, wenn der Befehl angegeben wird, aber keine Zuordnungsdaten in der Vignette vorhanden sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -Profil</span> </p></td> 
  <td class="stentry"> <p>Speichert eine Kopie des in der Vignette eingebetteten ICC-Profils in einer Datei. Es wird eine Warnmeldung erzeugt und es wird keine ICC-Profildatei erstellt, wenn der Befehl angegeben wird, aber kein ICC-Profil in der Vignette vorhanden ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramid</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine Pyramidenvignette. Erforderlich, wenn gerenderte Bilder mit Dynamic Media-Zoom-Viewern angezeigt werden sollen. Weitere Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Pixel-Breite und Höhenbegrenzung für das Miniaturbild. Wenn angegeben, wird ein JPEG-Bild, das nicht breiter und nicht größer als <span class="varname"> ival</span> ist, aus dem Vignettenansichtsbild, einem Bedienfeldbild der Kabinenstil-Datei oder der Beleuchtungskarte des ersten Stils in der Stildatei für Fensterbeleuchtung generiert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabevignettenbreiten in Pixel. Wird ignoriert, wenn <span class="codeph"> -info</span> angegeben ist. <span class="varname"> </span> ivalmay be 0, was die Höhe der Eingabevignette angibt. Detaillierte Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
</table>
