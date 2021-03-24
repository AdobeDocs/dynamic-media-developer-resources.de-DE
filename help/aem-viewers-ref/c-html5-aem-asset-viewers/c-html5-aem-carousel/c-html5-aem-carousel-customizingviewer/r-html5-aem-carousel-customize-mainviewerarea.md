---
description: Der Hauptbereich der Ansicht ist der Bereich, in dem sich das Karussellbannerbild befindet. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.
solution: Experience Manager
title: Hauptbereich des Viewers
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---


# Hauptviewer-Bereich{#main-viewer-area}

Der Hauptbereich der Ansicht ist der Bereich, in dem sich das Karussellbannerbild befindet. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.

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
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um einen Viewer mit einem weißen Hintergrund ( `#FFFFFF`) einzurichten und seine Größe 1174 x 500 Pixel festzulegen.

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```

