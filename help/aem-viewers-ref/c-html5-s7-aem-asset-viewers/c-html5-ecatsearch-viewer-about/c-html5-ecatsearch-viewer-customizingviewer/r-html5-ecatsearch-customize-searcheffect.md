---
description: Der Viewer zeigt Suchergebnisregionen über der Hauptversion an, um im Katalog gefundene Ansichten hervorzuheben.
seo-description: Der Viewer zeigt Suchergebnisregionen über der Hauptversion an, um im Katalog gefundene Ansichten hervorzuheben.
seo-title: Sucheffekt
solution: Experience Manager
title: Sucheffekt
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Sucheffekt{#search-effect}

Der Viewer zeigt Suchergebnisregionen über der Hauptversion an, um im Katalog gefundene Ansichten hervorzuheben.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild von Suchergebnisregionen wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrund der Suchergebnisregion. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Suchergebnisregionen mit einer halbtransparenten, gelben Füllung ein:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

