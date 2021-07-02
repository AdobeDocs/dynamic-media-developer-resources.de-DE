---
description: Die Hauptansicht besteht aus dem Rotationsbild, wenn das aktuelle Asset ein Rotationsset ist.
solution: Experience Manager
title: Rotationsansicht
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# Rotationsansicht{#spin-view}

Die Hauptansicht besteht aus dem Rotationsbild, wenn das aktuelle Asset ein Rotationsset ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format der Rotationsansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Rotationsansicht transparent zu machen.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
