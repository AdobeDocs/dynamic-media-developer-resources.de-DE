---
title: Haupt-Viewer-Bereich
description: Der Hauptansichtsbereich ist der Bereich, der vom Katalogbild eingenommen wird. Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9a37936b-ee3d-4ea0-9a86-ea14d0ef8be9
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Haupt-Viewer-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, der vom Katalogbild eingenommen wird. Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer
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
.s7ecatalogviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
