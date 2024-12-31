---
title: Zoom-Ansicht
description: Die Hauptansicht besteht aus dem vergrößerbaren Bild.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Zoom-Ansicht{#zoom-view}

Die Hauptansicht besteht aus dem vergrößerbaren Bild.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursor-</span> </p> </td> 
   <td colname="col2"> <p>Cursor über der Hauptansicht angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - , um die Hauptansicht transparent zu gestalten.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente `cursortype` Attributauswahl, die auf die `.s7zoomview` angewendet werden kann. Er steuert den Typ des Cursors auf der Grundlage des Komponentenstatus und der Benutzeraktion. Die folgenden `cursortype` werden unterstützt:

* `default`

  Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht zoombar ist.

* `zoomin`

  Wird angezeigt, wenn das Bild vergrößert werden kann.

* `reset`

  Wird angezeigt, wenn sich das Bild im maximalen Zoombereich befindet und auf den Ausgangszustand zurückgesetzt werden kann.

* `drag`

  Wird angezeigt, wenn der/die Benutzende das Bild schwenkt, das vergrößert ist.

* `slide`

  Wird angezeigt, wenn Benutzende durch horizontales Wischen oder Klicken einen Bildwechsel durchführen.
