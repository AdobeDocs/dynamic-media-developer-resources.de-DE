---
title: Indikator festlegen
description: Die Set-Anzeige ist eine Reihe von Punkten, die auf Farbfeldern gerendert werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Mithilfe der Punkte können Benutzer durch Seiten mit Miniaturen navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
TQID: 'https://experienceleague.adobe.com/y4QBgUjYMAh5-FlbA32Zgg0Peve1FcO-qhDxc0Ypv4M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 0%

---

# Indikator festlegen{#set-indicator}

Die Set-Anzeige ist eine Reihe von Punkten, die auf Farbfeldern gerendert werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Mithilfe der Punkte können Benutzer durch Seiten mit Miniaturen navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des festgelegten Indikators**

Das Erscheinungsbild des set indicator-Containers wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7zoomviewer .s7setindicator
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
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen Punkts für die Set-Anzeige wird mit dem CSS-Klassenselektor gesteuert:

`.s7zoomviewer .s7setindicator .s7dot`

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

Beispiel: So erstellen Sie einen festgelegten Indikatorpunkt von 15 x 15 Pixel mit einem horizontalen Rand von 2 Pixeln, einem oberen Rand von 5 Pixeln, einem unteren Rand von 1 Pixel, einem Radius von 12 Pixeln, #D5D3D3 Standardfarbe und #939393 aktiven Farbe:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```

