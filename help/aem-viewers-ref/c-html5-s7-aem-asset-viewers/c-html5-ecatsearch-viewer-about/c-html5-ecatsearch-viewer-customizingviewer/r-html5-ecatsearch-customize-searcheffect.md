---
title: Sucheffekt
description: Der Viewer zeigt Suchergebnisbereiche über der Hauptansicht an, um im Katalog gefundene Wörter oder Ausdrücke hervorzuheben.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# Sucheffekt{#search-effect}

Der Viewer zeigt Suchergebnisbereiche über der Hauptansicht an, um im Katalog gefundene Wörter oder Ausdrücke hervorzuheben.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild von Suchergebnisbereichen wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p>Hintergrund der Suchergebnisregion. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - zum Einrichten von Suchergebnisbereichen mit einer halbtransparenten, gelben Füllung:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
