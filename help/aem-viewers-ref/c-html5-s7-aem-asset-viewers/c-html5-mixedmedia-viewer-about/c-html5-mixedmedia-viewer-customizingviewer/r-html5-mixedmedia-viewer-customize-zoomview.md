---
description: Im kontinuierlichen Zoommodus besteht die Hauptansicht aus dem zoombaren Bild, wenn das aktuelle Asset ein einzelnes Bild ist.
solution: Experience Manager
title: Zoomansicht
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Zoomansicht{#zoom-view}

Im kontinuierlichen Zoommodus besteht die Hauptansicht aus dem zoombaren Bild, wenn das aktuelle Asset ein einzelnes Bild ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursor  </span> </p> </td> 
   <td colname="col2"> <p>Der Cursor wird über der Hauptansicht angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Zoomansicht transparent zu machen.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente die Attributauswahl `cursortype` , die auf die Klasse `.s7zoomview` angewendet werden kann. Er steuert den Typ des Cursors basierend auf dem Komponentenstatus und der Benutzeraktion. Die folgenden `cursortype` -Werte werden unterstützt:

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
