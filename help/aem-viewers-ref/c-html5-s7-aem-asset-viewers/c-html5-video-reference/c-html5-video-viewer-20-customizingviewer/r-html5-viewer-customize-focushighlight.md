---
title: Fokushervorhebung
description: Die Eingabefokushervorhebung, die um das Element der fokussierten Viewer-Benutzeroberfläche angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 9968c67b-02cc-4ac0-8ab1-c7eda565912d
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Fokushervorhebung{#focus-highlight}

Die Eingabefokushervorhebung, die um das Element der fokussierten Viewer-Benutzeroberfläche angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften**

Das Erscheinungsbild wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer *:focus
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
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Fokushervorhebung - Stil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel : Um die standardmäßige Browser-Fokushervorhebung für alle Elemente der Viewer-Benutzeroberfläche zu deaktivieren, fügen Sie die folgende CSS-Auswahl zum Stylesheet des Viewers hinzu:

```
.s7videoviewer *:focus { 
 outline: none; 
}
```
