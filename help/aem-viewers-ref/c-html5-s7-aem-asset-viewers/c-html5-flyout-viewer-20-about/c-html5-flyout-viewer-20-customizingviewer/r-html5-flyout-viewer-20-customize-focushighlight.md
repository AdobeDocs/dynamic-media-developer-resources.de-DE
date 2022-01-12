---
title: Fokushervorhebung
description: Die Hervorhebung des Eingabefokus, die um das fokussierte Element der Viewer-Benutzeroberfläche herum angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2cb2e719-ee56-45e5-a509-7e13bb3c2165
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Fokushervorhebung{#focus-highlight}

Die Hervorhebung des Eingabefokus, die um das fokussierte Element der Viewer-Benutzeroberfläche herum angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften**

Das Erscheinungsbild wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7flyoutviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> Entwurf </span> </p> </td> 
   <td colname="col2"> <p>Fokusmarkierungsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die standardmäßige Browserfokus-Hervorhebung für alle Elemente der Viewer-Benutzeroberfläche zu deaktivieren, fügen Sie den folgenden CSS-Selektor zum Stylesheet des Viewers hinzu:

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```
