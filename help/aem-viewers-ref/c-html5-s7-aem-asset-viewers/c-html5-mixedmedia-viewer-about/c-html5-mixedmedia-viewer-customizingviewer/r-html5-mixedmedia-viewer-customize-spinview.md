---
description: Die Ansicht "Main"besteht aus dem Rotationsbild, wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt.
solution: Experience Manager
title: Ansicht
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---


# Rotationsset-Ansicht{#spin-view}

Die Ansicht &quot;Main&quot;besteht aus dem Rotationsbild, wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt.

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
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat der Rotationsfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Ansicht transparent zu machen.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

