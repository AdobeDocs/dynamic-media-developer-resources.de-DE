---
description: Die Hauptansicht besteht aus dem statischen Bild.
solution: Experience Manager
title: Zoomansicht
feature: Dynamic Media Classic,Viewer,SDK/API,Interaktive Bilder
role: Developer,User
exl-id: e83d53a1-bee9-4e4d-8295-a3a350f3ff9c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---

# Zoomansicht{#zoom-view}

Die Hauptansicht besteht aus dem statischen Bild.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactiveimage .s7zoomview
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
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu machen.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```
