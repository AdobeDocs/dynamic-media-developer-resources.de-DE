---
description: Der Indikator "Festlegen"ist eine Reihe von Punkten, die am unteren Rand des Viewers gerendert werden. Es zeigt die aktuelle Position innerhalb des Satzes an.
seo-description: Der Indikator "Festlegen"ist eine Reihe von Punkten, die am unteren Rand des Viewers gerendert werden. Es zeigt die aktuelle Position innerhalb des Satzes an.
seo-title: Indikator festlegen
solution: Experience Manager
title: Indikator festlegen
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Indikator{#set-indicator} festlegen

Der Indikator &quot;Festlegen&quot;ist eine Reihe von Punkten, die am unteren Rand des Viewers gerendert werden. Es zeigt die aktuelle Position innerhalb des Satzes an.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Satzindikators**

Das Erscheinungsbild des Containers für den Set-Indikator wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p>Die Hintergrundfarbe im Hexadezimalformat des Satzindikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Indikator &quot;Festlegen&quot;unterstützt den Modus-Attributselektor, mit dem Sie verschiedene Stile für gepunktete und numerische Betriebsmodi anwenden können. Insbesondere entspricht `mode="numeric"` dem numerischen Betriebsmodus; `mode="dotted"` entspricht dem Standardpunktstatus.

Beispiel: So richten Sie einen Indikator mit einem weißen Hintergrund ein:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen Satzindikatorpunkts wird mit der CSS-Klassenauswahl gesteuert. Sie gilt für Elemente sowohl im gepunkteten als auch im numerischen Betriebsmodus.

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
   <td colname="col2"> <p>Breite des Punkts für den Indikator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des festgelegten Indikatorpunkts. </p> </td> 
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
   <td colname="col2"> <p>Hintergrundfarbe im Hexadezimalformat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Name der Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Schriftfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align  </span> </p> </td> 
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
>Die Elemente für die Einstellung unterstützen die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere entspricht `state="selected"` dem aktuellen Element im Satz; `state="unselected"` entspricht dem Standardelementstatus.

Beispiel: Zum Einrichten der Anzeige im gepunkteten Modus für Desktop-Systeme, die 20 Pixel vom unteren Rand des Viewers entfernt positioniert werden. Nicht ausgewählte Punkte sind schwarz mit 50 % Transparenz, 15 x 15 Pixel mit 7 Pixel abgerundeten Ecken. Die ausgewählten Punkte sind schwarz mit 90 % Transparenz, 18 x 18 Pixel mit 9 Pixel abgerundeten Ecken. Der Abstand zwischen Punkten beträgt 5 Pixel.

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

