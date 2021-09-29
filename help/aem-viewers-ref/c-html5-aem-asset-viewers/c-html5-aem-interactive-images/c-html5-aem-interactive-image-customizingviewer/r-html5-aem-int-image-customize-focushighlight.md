---
title: Fokushervorhebung
description: Die Hervorhebung des Eingabefokus, die um das fokussierte Element der Viewer-Benutzeroberfläche herum angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 89f34a96-2b21-4169-8c25-4b53005e59b8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Fokushervorhebung{#focus-highlight}

Die Hervorhebung des Eingabefokus, die um das fokussierte Element der Viewer-Benutzeroberfläche herum angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften**

Das Erscheinungsbild wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactiveimage *:focus
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
.s7interactiveimage *:focus { 
 outline: none; 
}
```
