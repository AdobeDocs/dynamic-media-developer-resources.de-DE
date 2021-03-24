---
description: Der Viewer zeigt Suchergebnisregionen über der Hauptversion an, um im Katalog gefundene Ansichten hervorzuheben.
solution: Experience Manager
title: Sucheffekt
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog-Suche
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 1%

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

