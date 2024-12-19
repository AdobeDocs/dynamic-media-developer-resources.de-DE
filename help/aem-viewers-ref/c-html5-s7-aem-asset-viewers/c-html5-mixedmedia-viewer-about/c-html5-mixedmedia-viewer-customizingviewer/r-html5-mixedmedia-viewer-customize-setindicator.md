---
title: Indikator festlegen
description: Die Set-Anzeige ist eine Reihe von Punkten, die auf den Hauptmustern gerendert werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Mithilfe der Punkte können Benutzer durch Seiten mit Miniaturen navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Indikator festlegen{#set-indicator}

Die Set-Anzeige ist eine Reihe von Punkten, die auf den Hauptmustern gerendert werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Mithilfe der Punkte können Benutzer durch Seiten mit Miniaturen navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des festgelegten Indikators**

Das Erscheinungsbild des set indicator-Containers wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7mixedmediaviewer .s7setindicator
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

Beispiel - So erstellen Sie einen Indikator mit einem weißen Hintergrund:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen Punkts für die Set-Anzeige wird mit dem CSS-Klassenselektor gesteuert:

`.s7mixedmediaviewer .s7setindicator .s7dot`

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
 </tbody> 
</table>

>[!NOTE]
>
>Der Punktindikator „Set Indicator“ unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichtszustände angewendet werden können. Insbesondere entspricht `state="selected"` der aktuellen Seite mit Miniaturen, `state="unselected"` dem standardmäßigen Punktstatus.

Beispiel: So erstellen Sie einen Indikatorpunkt von 15 x 15 Pixel mit einem horizontalen Rand von zwei Pixeln, einem oberen Rand von fünf Pixeln, einem unteren Rand von einem Pixel, einem Radius von 12 Pixeln, #D5D3D3 Standardfarbe und #939393 aktiven Farbe:

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
