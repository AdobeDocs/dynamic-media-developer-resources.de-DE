---
title: Hauptanzeige-Bereich
description: Der Hauptansichtsbereich ist der Bereich, der vom Karussellbannerbild belegt wird. Sie ist so eingestellt, dass sie an den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: bdac54f5-79e3-4d3d-9c7e-d9a7cec61c73
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Hauptanzeige-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, der vom Karussellbannerbild belegt wird. Sie ist so eingestellt, dass sie an den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7carouselviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Viewers mit weißem Hintergrund ( `#FFFFFF`) und seiner Größe 1174 x 500 Pixel.

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
