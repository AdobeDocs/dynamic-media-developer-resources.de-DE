---
description: Wenn Sie auf diese Schaltfläche klicken oder darauf tippen, kehrt ein Benutzer zur vorherigen Folie im Karussellsatz zurück. Diese Schaltfläche wird auf Touch-Geräten nicht angezeigt. Sie können diese Schaltfläche mit CSS skalieren, per Skin positionieren.
seo-description: Wenn Sie auf diese Schaltfläche klicken oder darauf tippen, kehrt ein Benutzer zur vorherigen Folie im Karussellsatz zurück. Diese Schaltfläche wird auf Touch-Geräten nicht angezeigt. Sie können diese Schaltfläche mit CSS skalieren, per Skin positionieren.
seo-title: Vorherige Folie
solution: Experience Manager
title: Vorherige Folie
topic: Dynamic media
uuid: 733fa270-ce95-4493-9d31-f7f638d8368d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 2%

---


# Vorherige Folie{#previous-slide}

Wenn Sie auf diese Schaltfläche klicken oder darauf tippen, kehrt ein Benutzer zur vorherigen Folie im Karussellsatz zurück. Diese Schaltfläche wird auf Touch-Geräten nicht angezeigt. Sie können diese Schaltfläche mit CSS skalieren, per Skin positionieren.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7carouselviewer .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position oben am Rand des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position rechts neben dem Viewer-Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position links neben dem Viewer-Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand des Viewer-Rahmens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursortyp. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md).

Beispiel: Zum Einrichten einer Schaltfläche für eine vorherige Folie, die 60 x 60 Pixel groß ist, 10 Pixel vom linken und vertikal zentrierten Rand des Viewers entfernt angeordnet ist und ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände anzeigt.

```
.s7carouselviewer .s7panleftbutton { 
 bottom: 50%; 
 left: 10px; 
 background-size:60px; 
 cursor: pointer; 
 } 
.s7carouselviewer.s7mouseinput .s7panleftbutton { 
 width:60px; 
 height:60px; 
 margin-bottom: -20px; 
} 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state]  { 
    background-image: url(../../viewers/s7viewers/html5/images/v2/CarouselDotsLeftButton_dark_sprite.png); 
} 
 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='up'] { background-position: -0px -60px;  } 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='over'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='down'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panleftbutton[state='disabled'] { background-position: -0px -60px; }
```

