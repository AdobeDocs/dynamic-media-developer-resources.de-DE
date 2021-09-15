---
title: Anzeige einstellen
description: Set Indicator ist eine Reihe von Punkten, die unten im Viewer gerendert werden. Sie zeigt die aktuelle Position innerhalb des Sets an.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---

# Anzeige einstellen{#set-indicator}

Set Indicator ist eine Reihe von Punkten, die unten im Viewer gerendert werden. Sie zeigt die aktuelle Position innerhalb des Sets an.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Set Indicators**

Das Erscheinungsbild des set-Indikator-Containers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7carouselviewer .s7setindicator
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe im hexadezimalen Format des Set-Indikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Festlegen-Indikator unterstützt die Modusattributauswahl, mit der Sie verschiedene Stile für gepunktete und numerische Vorgangsmodi anwenden können. Insbesondere entspricht `mode="numeric"` dem numerischen Betriebsmodus; `mode="dotted"` entspricht dem Standardpunktstatus.

Angenommen, Sie möchten einen Indikator mit weißem Hintergrund einrichten:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen festgelegten Anzeigepunkts wird mit der CSS-Klassenauswahl gesteuert. Sie gilt für Elemente sowohl im gepunkteten als auch im numerischen Betriebsmodus.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des festgelegten Anzeigepunkts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des festgelegten Anzeigepunkts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p>Linker Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p>Oberer Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>Rechter Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Unterer Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Rahmenradius in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe im hexadezimalen Format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p>Name der Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Schriftfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertikale Ausrichtung  </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Ausrichtung des Bannerindex. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>Texthöhe für den Bannerindex. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die Festlegen-Indikatorelemente unterstützen die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere entspricht `state="selected"` dem aktuellen Element im Satz; `state="unselected"` entspricht dem standardmäßigen Elementstatus.

Angenommen, Sie möchten eine Set-Anzeige im gepunkteten Modus für Desktop-Systeme einrichten. Sie möchten, dass sie 20 Pixel vom unteren Rand des Viewers entfernt wird. Und Sie möchten, dass nicht ausgewählte Punkte schwarz mit 50 % Transparenz, 15 x 15 Pixel mit sieben Pixel abgerundeten Ecken sind. Ausgewählte Punkte sind schwarz mit 90 % Transparenz, 18 x 18 Pixel mit neun abgerundeten Ecken. Der Abstand zwischen Punkten beträgt fünf Pixel.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
