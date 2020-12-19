---
description: Die Ansicht besteht hauptsächlich aus dem Zoombild.
seo-description: Die Ansicht besteht hauptsächlich aus dem Zoombild.
seo-title: Zoom-Ansicht
solution: Experience Manager
title: Zoom-Ansicht
topic: Dynamic media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Zoom-Ansicht{#zoom-view}

Die Ansicht besteht hauptsächlich aus dem Zoombild.

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format der Haupt-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Der Cursor wird über der Haupt-Ansicht angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Ansicht transparent zu machen.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente die Attributauswahl `cursortype`, die auf die Klasse `.s7zoomview` angewendet werden kann. Er steuert den Typ des Cursors basierend auf dem Komponentenstatus und der Benutzeraktion. Die folgenden `cursortype`-Werte werden unterstützt:

* `default`

   Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht gezoombar ist.

* `zoomin`

   Wird angezeigt, wenn das Bild vergrößert werden kann.

* `reset`

   Wird angezeigt, wenn das Bild den maximalen Zoomgrad erreicht hat und auf den Ausgangszustand zurückgesetzt werden kann.

* `drag`

   Wird angezeigt, wenn der Benutzer das Bild verschiebt, das gezoomt ist.

* `slide`

   Wird angezeigt, wenn der Benutzer einen Bildtausch durch horizontales Blättern oder Klick durchführt.

