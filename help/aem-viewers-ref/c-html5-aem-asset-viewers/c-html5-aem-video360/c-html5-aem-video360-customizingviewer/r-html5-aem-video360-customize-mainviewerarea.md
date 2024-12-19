---
title: Haupt-Viewer-Bereich
description: Der Hauptansichtsbereich ist der Bereich, in dem sich das 360-Grad-Video befindet. Er wird so eingestellt, dass er auf den Bildschirm des verfügbaren Geräts passt, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 912cb4b3-6409-48ed-9b9c-968b63718a1b
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# Haupt-Viewer-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, in dem sich das 360-Grad-Video befindet. Er wird so eingestellt, dass er auf den Bildschirm des verfügbaren Geräts passt, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer
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

## Beispiel {#section-ee18025b182a42dc98052de5f133ddfe}

Zum Einrichten eines Viewers mit einem weißen Hintergrund ( `#FFFFFF`) und Festlegen seiner Größe auf 512 x 288 Pixel.

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
