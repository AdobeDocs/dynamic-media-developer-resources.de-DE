---
description: Set Indicator ist eine Reihe von Punkten, die auf Hauptmustern gerendert werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Die Punkte helfen Benutzern, durch Seiten von Miniaturansichten zu navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.
solution: Experience Manager
title: Anzeige einstellen
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# Anzeige einstellen{#set-indicator}

Set Indicator ist eine Reihe von Punkten, die auf Hauptmustern gerendert werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Die Punkte helfen Benutzern, durch Seiten von Miniaturansichten zu navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Set Indicators**

Das Erscheinungsbild des set-Indikator-Containers wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe im hexadezimalen Format des Set-Indikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Set-Indikators mit weißem Hintergrund:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen festgelegten Anzeigepunkts wird mit der CSS-Klassenauswahl gesteuert:

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
 </tbody> 
</table>

>[!NOTE]
>
>Der Set Indicator Punkt unterstützt die Attributauswahl `state`, die verwendet werden kann, um verschiedene Skins auf verschiedene Miniaturansichten anzuwenden. Insbesondere `state="selected"` entspricht der aktuellen Seite der Miniaturansichten, `state="unselected"` entspricht dem Standardpunktstatus.

Beispiel: Um einen festgelegten Anzeigepunkt auf 15 x 15 Pixel festzulegen, mit zwei Pixel horizontaler Rand, fünf Pixel oberer Rand, einem Pixel unteren Rand, zwölf Pixel Radius, #D5D3D3 Standardfarbe und #9393 aktiver Farbe:

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
