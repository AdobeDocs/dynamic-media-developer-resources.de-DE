---
title: Indikator festlegen
description: Ein Indikator für ein Set ist eine Reihe von Punkten, die am unteren Rand des Viewers gerendert werden. Zeigt die aktuelle Position innerhalb des Sets an.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Indikator festlegen{#set-indicator}

Ein Indikator für ein Set ist eine Reihe von Punkten, die am unteren Rand des Viewers gerendert werden. Zeigt die aktuelle Position innerhalb des Sets an.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des festgelegten Indikators**

Das Erscheinungsbild des set indicator-Containers wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe im Hexadezimalformat des eingestellten Indikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Indikator „Set“ unterstützt die Modusattribut-Auswahl, mit der Sie verschiedene Stile für gepunktete und numerische Betriebsmodi anwenden können. Insbesondere entspricht `mode="numeric"` dem numerischen Betriebsmodus; `mode="dotted"` entspricht dem Standard-Punktzustand.

Angenommen, Sie möchten einen Indikator mit einem weißen Hintergrund einrichten:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen Punkts für die Set-Anzeige wird mit dem CSS-Klassenselektor gesteuert. Dies gilt sowohl für Elemente im gepunkteten als auch für numerische Betriebsarten.

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
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des eingestellten Indikatorpunkts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des eingestellten Indikatorpunkts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand links </span> </p> </td> 
   <td colname="col2"> <p>Linker Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Oberer Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand rechts </span> </p> </td> 
   <td colname="col2"> <p>Rechter Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand unten </span> </p> </td> 
   <td colname="col2"> <p>Unterer Rand in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmenradius in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe im Hexadezimalformat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Name der Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> zur vertikalen Ausrichtung <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Vertikale Ausrichtung des Bannerindexes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> mit <span class="codeph"> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p>Texthöhe für den Bannerindex. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Set Indicator-Elemente unterstützen die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere entspricht `state="selected"` dem aktuellen Element im Satz; `state="unselected"` entspricht dem Standardelement-Status.

Angenommen, Sie möchten für Desktop-Systeme einen Indikator im gepunkteten Modus einrichten. Sie möchten, dass sie 20 Pixel vom unteren Rand des Viewers entfernt positioniert wird. Außerdem sollen nicht ausgewählte Punkte schwarz mit 50 % Transparenz, 15 x 15 Pixel mit sieben Pixel mit abgerundeten Ecken sein. Ausgewählte Punkte sind schwarz mit 90 % Transparenz, 18 x 18 Pixel mit neun Pixel abgerundeten Ecken. Der Abstand zwischen Punkten beträgt fünf Pixel.

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
