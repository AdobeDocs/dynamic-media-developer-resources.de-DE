---
title: Hauptanzeige-Bereich
description: Der Hauptansichtsbereich ist der Bereich, der vom Zoombild und den Farbfeldern belegt ist. Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# Hauptanzeige-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, der vom Zoombild und den Farbfeldern belegt ist. Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Bei der Arbeit im eingebetteten Modus (wenn dem Hauptansichtsbereich eine explizite Größe zugewiesen wird) verringert der Viewer automatisch die Höhe seines Hauptbereichs um die Höhe der Farbfeldkomponente, die mit dem einzelnen Bild arbeitet. Daher sind keine Farbfelder erforderlich.

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Viewers mit weißem Hintergrund ( `#FFFFFF`) und machen Sie ihre Größe 512 x 288 Pixel.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
