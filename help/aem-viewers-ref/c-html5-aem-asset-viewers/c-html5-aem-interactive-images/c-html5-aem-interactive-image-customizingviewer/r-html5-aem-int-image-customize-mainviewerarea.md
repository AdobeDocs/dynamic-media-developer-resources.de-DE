---
description: Der Hauptbereich der Ansicht ist der Bereich, in dem sich das Zoombild befindet. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.
seo-description: Der Hauptbereich der Ansicht ist der Bereich, in dem sich das Zoombild befindet. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.
seo-title: Hauptbereich des Viewers
solution: Experience Manager
title: Hauptbereich des Viewers
uuid: 666328fe-1819-43a6-a2c2-ba63ac798700
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Bilder
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Hauptviewer-Bereich{#main-viewer-area}

Der Hauptbereich der Ansicht ist der Bereich, in dem sich das Zoombild befindet. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactiveimage
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
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```

