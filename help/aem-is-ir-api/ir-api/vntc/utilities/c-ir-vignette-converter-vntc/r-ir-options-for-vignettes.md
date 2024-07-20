---
description: Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.
solution: Experience Manager
title: Optionen für Vignetten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Optionen für Vignetten{#options-for-vignettes}

Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine XML-Datei, die die Objekthierarchie einschließlich der ausgewählten Objektattribute darstellt. Der Inhalt der Datei entspricht dem vom Befehl <span class="codeph"> req=contents</span> zurückgegebenen Inhalt. Die Datei hat denselben Namen wie die Quelldatei, jedoch mit dem Suffix <span class="filepath"> .xml</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Schneiden Sie die Vignette vor der Skalierung zu. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> y</span></span> ist die obere linke Ecke des Zuschnittrechtecks und <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> ist die Größe des Zuschnittrechtecks. Die Werte sind Pixelkoordinaten, die relativ zum Vollbildansicht der Quellvignette sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-beschneiden <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Schneiden Sie die Vignette vor der Skalierung zu. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> ist die obere linke Ecke des Zuschnittrechtecks und <span class="codeph"><span class="varname"> widmet sich </span>,<span class="varname"> hein</span></span> der Größe des Zuschnittrechtecks. Die Werte werden relativ zum Ansichtsbild der Quellvignette normalisiert und müssen zwischen 0,0...1.0 liegen. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> und <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> dürfen nicht größer als 1,0 sein. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>Bewahren Sie eingebettete Materialien in der Vignette auf. Standardmäßig werden Materialien aus der Vignette entfernt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabevignettenhöhen in Pixel. Wird ignoriert, wenn -info angegeben ist. <span class="varname"> ival</span> kann 0 betragen, was die Breite der Eingabevignette angibt. Detaillierte Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Aktivieren Sie die Extraktion der Imagemap-Datei aus der Vignette. Die Zuordnungsdaten werden in eine HTML-Datei geschrieben, die nur ein <span class="codeph"> &lt;map&gt;</span> -Element enthält. Die Ausgabedatei hat denselben Namen wie die Ausgabebilddatei, allerdings mit dem Suffix <span class="filepath"> .htm</span>. Es wird eine Warnmeldung erzeugt und keine Datei erstellt, wenn der Befehl angegeben wird, aber keine Zuordnungsdaten in der Vignette vorhanden sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Speichert eine Kopie des in der Vignette eingebetteten ICC-Profils in einer Datei. Es wird eine Warnmeldung erzeugt und es wird keine ICC-Profildatei erstellt, wenn der Befehl angegeben wird, aber kein ICC-Profil in der Vignette vorhanden ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramid</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine Pyramidenvignette. Erforderlich, wenn gerenderte Bilder mit Dynamic Media-Zoom-Viewern angezeigt werden sollen. Weitere Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Pixel-Breite und Höhenbegrenzung für das Miniaturbild. Wenn angegeben, wird ein JPEG-Bild, das nicht breiter und nicht größer als <span class="varname"> ival</span> ist, aus dem Vignettenansichtsbild, einem Bedienfeldbild der Kabinenstil-Datei oder der Beleuchtungskarte des ersten Stils in der Stildatei für Fensterbeleuchtung generiert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabevignetten-Breiten in Pixel. Wird ignoriert, wenn <span class="codeph"> -info</span> angegeben ist. <span class="varname"> ival</span> kann 0 sein, was die Höhe der Eingabevignette angibt. Detaillierte Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
</table>
