---
title: Zoomansicht
description: Die Hauptansicht besteht aus dem zoombaren Bild.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Zoomansicht{#zoom-view}

Die Hauptansicht besteht aus dem zoombaren Bild.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7zoomviewer .s7zoomview
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

Beispiel - Um die Hauptansicht transparent zu machen.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente `cursortype` -Attributauswahl, die auf die `.s7zoomview` -Klasse. Er steuert den Typ des Cursors basierend auf dem Komponentenstatus und der Benutzeraktion. Folgendes `cursortype` -Werte werden unterstützt:

* `default`

   Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht vergrößert werden kann.

* `zoomin`

   Wird angezeigt, wenn das Bild vergrößert werden kann.

* `reset`

   Wird angezeigt, wenn sich das Bild auf einem maximalen Zoomfaktor befindet und auf seinen ursprünglichen Status zurückgesetzt werden kann.

* `drag`

   Wird angezeigt, wenn der Benutzer das Bild schaltet, das gezoomt ist.

* `slide`

   Wird angezeigt, wenn der Benutzer einen Bildtausch durch horizontales Wischen oder Klick durchführt.
