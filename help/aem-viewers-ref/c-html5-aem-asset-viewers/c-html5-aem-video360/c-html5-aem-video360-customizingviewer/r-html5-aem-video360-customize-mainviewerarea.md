---
description: Der Hauptbereich der Ansicht ist der Bereich, der von dem 360-Video belegt wird. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.
seo-description: Der Hauptbereich der Ansicht ist der Bereich, der von dem 360-Video belegt wird. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.
seo-title: Hauptbereich des Viewers
solution: Experience Manager
title: Hauptbereich des Viewers
topic: Dynamic media
uuid: ec321901-f077-4f71-a48c-20cae11c41d1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# Hauptviewer-Bereich{#main-viewer-area}

Der Hauptbereich der Ansicht ist der Bereich, der von dem 360-Video belegt wird. Normalerweise wird sie auf den verfügbaren Gerätebildschirm eingestellt, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer
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
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-ee18025b182a42dc98052de5f133ddfe}

Um einen Viewer mit einem weißen Hintergrund ( `#FFFFFF`) einzurichten und seine Größe 512 x 288 Pixel festzulegen.

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

