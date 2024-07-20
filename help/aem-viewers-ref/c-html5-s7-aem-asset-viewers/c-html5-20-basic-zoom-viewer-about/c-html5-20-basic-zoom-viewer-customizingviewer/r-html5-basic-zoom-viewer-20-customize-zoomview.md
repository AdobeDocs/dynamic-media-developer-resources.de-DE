---
title: Zoom-Ansicht
description: Die Hauptansicht besteht aus dem zoombaren Bild.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---

# Zoom-Ansicht{#zoom-view}

Die Hauptansicht besteht aus dem zoombaren Bild.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursor </span> </p> </td> 
   <td colname="col2"> <p>Der Cursor wird über der Hauptansicht angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu machen.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente die Attributauswahl `cursortype` , die auf die Klasse `.s7zoomview` angewendet werden kann, und steuert den Cursortyp basierend auf dem Komponentenstatus und der Benutzeraktion. Die folgenden `cursortype` -Werte werden unterstützt:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wert </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn sich das Bild auf einem maximalen Zoomfaktor befindet und auf seinen ursprünglichen Status zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ziehen </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn ein Benutzer das Bild schaltet, das gezoomt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>
