---
title: Haupt-Viewer-Bereich
description: Der Hauptansichtsbereich ist der Bereich, in dem sich das Zoombild und die Farbfelder befinden. Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Haupt-Viewer-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, in dem sich das Zoombild und die Farbfelder befinden. Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Beim Arbeiten im eingebetteten Modus (wenn dem Haupt-Viewer-Bereich eine explizite Größe zugewiesen wird) verringert der Viewer automatisch die Höhe seines Hauptbereichs um die Höhe der Farbfeld-Komponente, die mit dem einzelnen Bild arbeitet. Daher sind Farbfelder nicht erforderlich.

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Ein Viewer mit einem weißen Hintergrund ( `#FFFFFF`) wird eingerichtet und auf 512 x 288 Pixel festgelegt.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
