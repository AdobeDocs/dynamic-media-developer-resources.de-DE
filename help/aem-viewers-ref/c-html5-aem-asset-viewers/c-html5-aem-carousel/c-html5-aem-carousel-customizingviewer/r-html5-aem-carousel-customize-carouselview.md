---
description: Die Hauptansicht besteht aus dem Bannerbild.
solution: Experience Manager
title: Karussellansicht
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: aa41b209-11c7-4744-aaa5-dc0b503607c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---

# Karussellansicht{#carousel-view}

Die Hauptansicht besteht aus dem Bannerbild.

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
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu machen.

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```
