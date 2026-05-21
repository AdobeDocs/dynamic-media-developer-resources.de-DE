---
title: Zoom-Ansicht
description: Im kontinuierlichen Zoom-Modus besteht die Hauptansicht aus dem zoombaren Bild, wenn das aktuelle Asset ein einzelnes Bild ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
TQID: 'https://experienceleague.adobe.com/xfQKn46HParEFKYh1jrrVxbmkUKQHJbcWlJ7LWHIsc0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# Zoom-Ansicht{#zoom-view}

Im kontinuierlichen Zoom-Modus besteht die Hauptansicht aus dem zoombaren Bild, wenn das aktuelle Asset ein einzelnes Bild ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursor-</span> </p> </td> 
   <td colname="col2"> <p>Cursor über der Hauptansicht angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - , um die Zoom-Ansicht transparent zu machen.

```
.s7mixedmediaviewer .s7zoomview { 
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
