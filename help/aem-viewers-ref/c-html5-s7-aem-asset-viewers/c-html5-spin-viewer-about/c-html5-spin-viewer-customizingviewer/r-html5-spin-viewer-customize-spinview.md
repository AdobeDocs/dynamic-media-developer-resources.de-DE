---
description: Die Ansicht besteht hauptsächlich aus dem Rotationsbild.
seo-description: Die Ansicht besteht hauptsächlich aus dem Rotationsbild.
seo-title: Ansicht
solution: Experience Manager
title: Ansicht
topic: Dynamic media
uuid: 74f42373-b08c-43c8-8f08-e61a09655b61
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---


# Rotationsset-Ansicht{#spin-view}

Die Ansicht besteht hauptsächlich aus dem Rotationsbild.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7spinviewer .s7spinview
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
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```

