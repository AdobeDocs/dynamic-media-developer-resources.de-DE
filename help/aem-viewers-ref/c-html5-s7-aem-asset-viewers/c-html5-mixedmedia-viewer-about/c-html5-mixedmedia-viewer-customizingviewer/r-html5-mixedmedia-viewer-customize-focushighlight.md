---
description: Die Hervorhebung des Eingabefokus, die um das fokussierte Viewer-UI-Element angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.
seo-description: Die Hervorhebung des Eingabefokus, die um das fokussierte Viewer-UI-Element angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.
seo-title: Fokushervorhebung
solution: Experience Manager
title: Fokushervorhebung
topic: Dynamic Media
uuid: e7be5ad0-f27b-4e00-a3cc-e053d924b69d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---


# Fokusmarkierung{#focus-highlight}

Die Hervorhebung des Eingabefokus, die um das fokussierte Viewer-UI-Element angezeigt wird, wird mit der CSS-Klassenauswahl gesteuert.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften**

Das Erscheinungsbild wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> Umriss  </span> </p> </td> 
   <td colname="col2"> <p>Fokusmarkierungsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die standardmäßige Browserfokushervorhebung für alle Elemente der Benutzeroberfläche des Viewers zu deaktivieren, fügen Sie den folgenden CSS-Selektor zum Stylesheet des Viewers hinzu:

```
.s7mixedmediaviewer *:focus { 
 outline: none; 
}
```

