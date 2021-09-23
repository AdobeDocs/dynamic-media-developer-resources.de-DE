---
title: Fokushervorhebung
description: Die Hervorhebung des Eingabefokus, die um das fokussierte Benutzeroberflächenelement des Viewers herum angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: cb5231ed-106a-444f-aac7-06dd1a84a665
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# Fokushervorhebung{#focus-highlight}

Die Hervorhebung des Eingabefokus, die um das fokussierte Benutzeroberflächenelement des Viewers herum angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften**

Das Erscheinungsbild wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> Entwurf  </span> </p> </td> 
   <td colname="col2"> <p>Fokusmarkierungsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die standardmäßige Browserfokus-Hervorhebung für alle Elemente der Viewer-Benutzeroberfläche zu deaktivieren, fügen Sie den folgenden CSS-Selektor zum Stylesheet des Viewers hinzu:

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```
