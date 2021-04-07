---
description: Die Hauptansicht besteht aus der Ansicht des Banners.
solution: Experience Manager
title: Karussell-Ansicht
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
exl-id: aa41b209-11c7-4744-aaa5-dc0b503607c6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---

# Karussell-Ansicht{#carousel-view}

Die Hauptansicht besteht aus der Ansicht des Banners.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7carouselviewer .s7carouselview
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
 </tbody> 
</table>

Beispiel - um die Ansicht transparent zu machen.

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```
