---
description: Der Hauptansichtsbereich ist der Bereich, der von der Hauptansicht und den Farbfeldern belegt ist. Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.
solution: Experience Manager
title: Hauptanzeige-Bereich
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: fe8b748c-5318-4fcd-9f3a-d50523bb3f8f
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# Hauptanzeige-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, der von der Hauptansicht und den Farbfeldern belegt ist. Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer 
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um einen Viewer mit weißem Hintergrund ( `#FFFFFF`) einzurichten und seine Größe 512 x 288 Pixel zu ändern.

```
.s7mixedmediaviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
