---
description: Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.
seo-description: Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.
seo-title: Optionen für Vignetten
solution: Experience Manager
title: Optionen für Vignetten
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Optionen für Vignetten{#options-for-vignettes}

Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn sourceFile keine Vignette ist.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -Inhalt</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine XML-Datei, die die Objekthierarchie einschließlich der ausgewählten Objektattribute darstellt. Der Inhalt der Datei ist identisch mit dem vom Befehl <span class="codeph"> req=contents</span> zurückgegebenen Inhalt. Die Datei hat denselben Namen wie die Quelldatei, jedoch mit dem Suffix <span class="filepath"> .xml</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-beschneiden <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Beschneiden der Vignette vor der Skalierung. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> ist die obere linke Ecke des Rechtecks, und <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> ist die Größe des Rechtecks. Die Werte sind Pixelkoordinaten relativ zum Bild der Ansicht der Quellvignette mit voller Auflösung. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-ocn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Beschneiden der Vignette vor der Skalierung. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> ist die obere linke Ecke des Rechtecks des Beschneidungsrechtecks, und die <span class="codeph"><span class="varname"> Breite</span>,<span class="varname"> also</span></span> die Größe des Rechtecks. Die Werte werden relativ zum Bild der Ansicht der Quell-Vignette normalisiert und müssen zwischen 0,0...1.0 liegen. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> und <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> dürfen nicht größer als 1,0 sein. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -Einbettmaterialien</span> </p></td> 
  <td class="stentry"> <p>Bewahren Sie eingebettete Materialien in der Vignette für die Ausgabe auf. Standardmäßig werden Materialien aus der Vignette entfernt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabevignettenhöhen in Pixel. Wird ignoriert, wenn -info angegeben ist. <span class="varname"> ival</span> kann 0 sein, was die Breite der Vignette angibt. Detaillierte Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Aktivieren Sie die Extraktion der Imagemap-Datei aus der Vignette. Die Zuordnungsdaten werden in eine HTML-Datei geschrieben, die nur ein <span class="codeph"> &lt;map&gt;</span> -Element enthält. Die Ausgabedatei hat denselben Namen wie die Ausgabebilddatei, allerdings mit dem Suffix <span class="filepath"> .htm</span> . Es wird eine Warnmeldung generiert und keine Datei erstellt, wenn der Befehl angegeben wurde, aber keine Zuordnungsdaten in der Vignette vorhanden sind. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -Profil</span> </p></td> 
  <td class="stentry"> <p>Speichert eine Kopie des in die Vignette eingebetteten ICC-Profils in einer Datei. Es wird eine Warnmeldung generiert und es wird keine ICC-Profil-Datei erstellt, wenn der Befehl angegeben wurde, aber kein ICC-Profil in der Vignette vorhanden ist. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramide</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine Pyramidenvignette. Erforderlich, wenn gerenderte Bilder mit Scene7-Zoom-Viewern angezeigt werden sollen. Weitere Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Begrenzung der Pixelbreite und -höhe für das Miniaturbild. Falls angegeben, wird ein JPEG-Ansicht, das nicht breiter und nicht größer als <span class="varname"> ival</span> ist, aus dem Vignettenbild, einem Bereichsbild der Möbeldatei oder der Beleuchtungskarte des ersten Stils in der Stildatei für Fensterbeläge generiert. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabe-Vignettenbreiten in Pixel. Wird ignoriert, wenn <span class="codeph"> -info</span> angegeben ist. <span class="varname"> ival</span> kann 0 betragen, was die Höhe der Vignette angibt. Detaillierte Informationen finden Sie unter <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> . </p></td> 
 </tr> 
</table>

