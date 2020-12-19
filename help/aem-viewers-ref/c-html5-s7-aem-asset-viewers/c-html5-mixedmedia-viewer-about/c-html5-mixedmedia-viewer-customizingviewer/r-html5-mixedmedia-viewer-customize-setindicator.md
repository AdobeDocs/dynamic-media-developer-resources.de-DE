---
description: '"Sset-Indikator"ist eine Reihe von Punkten, die auf den Hauptfeldern dargestellt werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Die Punkte helfen Benutzern, durch die Seiten von Miniaturbildern zu navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.'
seo-description: '"Sset-Indikator"ist eine Reihe von Punkten, die auf den Hauptfeldern dargestellt werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Die Punkte helfen Benutzern, durch die Seiten von Miniaturbildern zu navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.'
seo-title: Indikator festlegen
solution: Experience Manager
title: Indikator festlegen
topic: Dynamic media
uuid: e62fac7c-28b6-40bf-83cc-8bcfbaa0dfa3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 1%

---


# Indikator{#set-indicator} festlegen

&quot;Sset-Indikator&quot;ist eine Reihe von Punkten, die auf den Hauptfeldern dargestellt werden, wenn ein Viewer auf einem Touch-Gerät verwendet wird. Die Punkte helfen Benutzern, durch die Seiten von Miniaturbildern zu navigieren, wenn keine Bildlaufschaltflächen verfügbar sind.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Satzindikators**

Das Erscheinungsbild des Containers für den Set-Indikator wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p>Die Hintergrundfarbe im Hexadezimalformat des Satzindikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie einen Indikator mit einem weißen Hintergrund ein:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

Das Erscheinungsbild eines einzelnen Datensatzindikatorpunkts wird mit der CSS-Klassenauswahl gesteuert:

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
 </tbody> 
</table>

>[!NOTE]
>
>Der Anzeigepunkt &quot;Festlegen&quot;unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere entspricht `state="selected"` der aktuellen Seite der Miniaturansichten, `state="unselected"` dem Standardpunktstatus.

Beispiel: Um den Anzeigepunkt auf 15 x 15 Pixel mit zwei Pixel horizontalem Rand, fünf Pixel oberem Rand, einem Pixel unteren Rand, zwölf Pixel Radius, #D5D3D3-Standardfarbe und #939393 zu setzen, legen Sie folgende Farbe fest:

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

