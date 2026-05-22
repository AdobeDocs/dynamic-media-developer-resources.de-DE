---
description: Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn „sourceFile“ keine Vignette ist.
solution: Experience Manager
title: Optionen für Vignetten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
TQID: 'https://experienceleague.adobe.com/f9Fkiw7Rxx8O0tLFlmnfETYXNNHI7Yui-2t2lNegrIM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 462
ht-degree: 0%

---

# Optionen für Vignetten{#options-for-vignettes}

Die folgenden Optionen steuern die Verarbeitung von Vignettendateien. Sie werden ignoriert, wenn „sourceFile“ keine Vignette ist.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine XML-Datei, die die Objekthierarchie darstellt und ausgewählte Objektattribute enthält. Der Inhalt der Datei entspricht dem vom Befehl <span class="codeph"> req=contents zurückgegebenen </span>. Die Datei hat denselben Namen wie die Quelldatei, jedoch mit dem Suffix <span class="filepath">.xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-Crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Beschneiden Sie die Vignette vor der Skalierung. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> ist die obere linke Ecke des Zuschnittsrechtecks und <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> ist die Größe des Zuschnittsrechtecks. Die Werte sind Pixelkoordinaten relativ zum Ansichtsbild mit voller Auflösung der Quellvignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-Crop <span class="varname"> XN</span><span class="varname"> YN</span><span class="varname"> Wind</span><span class="varname"> Hein</span></span> </p> </td> 
  <td class="stentry"> <p>Beschneiden Sie die Vignette vor der Skalierung. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> ist die obere linke Ecke des Zuschnittsrechtecks und <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hein</span></span> ist die Größe des Zuschnittsrechtecks. Die Werte werden relativ zum Ansichtsbild der Quellvignette normalisiert und müssen zwischen 0,0 und 1,0 liegen. </p> <p><span class="codeph"><span class="varname"> XN</span></span>+<span class="codeph"><span class="varname"> Wind</span></span> und <span class="codeph"><span class="varname"> YN</span></span>+<span class="codeph"><span class="varname"> Hein</span></span> dürfen nicht größer als 1,0 sein. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedMaterials</span> </p></td> 
  <td class="stentry"> <p>Beibehaltung der eingebetteten Materialien in der Vignette. Standardmäßig werden Materialien aus der Vignette entfernt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Höhe <span class="varname"> Rivalen</span></span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Ausgabehöhen der Vignette in Pixel. Ignoriert, wenn -info angegeben ist. <span class="varname"> ival</span> kann 0 sein, was die Breite der Eingangsvignette angibt. Siehe <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> für detaillierte Informationen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Aktivieren Sie die Extraktion der Imagemap-Datei aus der Vignette. Die Zuordnungsdaten werden in eine HTML-Datei geschrieben, die nur ein <span class="codeph"> &lt;map&gt;</span> enthält. Die Ausgabedatei erhält denselben Namen wie die Ausgabedatei, weist jedoch die Dateiendung <span class="filepath">htm</span> auf. Wenn der Befehl angegeben wird, aber keine Zuordnungsdaten in der Vignette vorhanden sind, wird eine Warnmeldung generiert und keine Datei erstellt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Speichert eine Kopie des in die Vignette eingebetteten ICC-Profils in einer Datei. Wenn der Befehl angegeben wird, aber kein ICC-Profil in der Vignette vorhanden ist, wird eine Warnmeldung generiert und keine ICC-Profildatei erstellt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramide</span> </p></td> 
  <td class="stentry"> <p>Erstellt eine Pyramidenvignette. Erforderlich, wenn gerenderte Bilder mit Dynamic Media-Zoom-Viewern angezeigt werden sollen. Siehe <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> für weitere Informationen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ThumbWidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Pixelbreite und -höhe für das Miniaturbild. Wenn angegeben, wird aus dem Vignettenansichtsbild, einem Bereichsbild der Schrankstildatei oder der Beleuchtungskarte <span class="varname"> ersten Stils in der Fensterabdeckungsstildatei ein JPEG-Bild generiert, das nicht breiter und nicht größer als Rival </span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Eine oder mehrere Vignettenbreiten in Pixel. Ignoriert, wenn <span class="codeph"> -info</span> angegeben ist. <span class="varname"> ival</span> kann 0 sein, was die Höhe der Eingangsvignette angibt. Siehe <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignettenskalierung</a> für detaillierte Informationen. </p></td> 
 </tr> 
</table>
