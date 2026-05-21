---
title: Haupt-Viewer-Bereich
description: Der Hauptansichtsbereich ist der Bereich, der vom Zoombild eingenommen wird. Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f51de2d6-0de2-4a4d-bbf4-185547e6c550
TQID: 'https://experienceleague.adobe.com/YvcGhESFPYLw7zovIb2EDBdQ75vdzC4C7mgRUZsD9QU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 0%

---

# Haupt-Viewer-Bereich{#main-viewer-area}

Der Hauptansichtsbereich ist der Bereich, der vom Zoombild eingenommen wird. Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7basiczoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Einrichten eines Viewers mit weißem Hintergrund ( `#FFFFFF`) und Festlegen seiner Größe auf 512 x 288 Pixel.

```
.s7basiczoomviewer{ 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
