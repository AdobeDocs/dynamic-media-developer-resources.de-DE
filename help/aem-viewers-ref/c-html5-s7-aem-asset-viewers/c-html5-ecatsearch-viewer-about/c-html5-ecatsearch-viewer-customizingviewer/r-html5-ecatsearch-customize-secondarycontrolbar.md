---
title: Sekundärer Steuerbalken
description: Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen Erste und Letzte Seite sowie einen Seitenindikator enthält, wenn er in CSS zur Verfügung gestellt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Sekundärer Steuerbalken{#secondary-control-bar}

Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen Erste und Letzte Seite sowie einen Seitenindikator enthält, wenn er in CSS zur Verfügung gestellt wird.

Standardmäßig wird sie nur auf Smartphones im unteren Bereich des Viewers angezeigt. Es wird immer die gesamte verfügbare Viewer-Breite benötigt. Es ist möglich, die Farbe, Höhe und vertikale Position durch CSS relativ zum Viewer-Container zu ändern.

Das Erscheinungsbild der sekundären Steuerleiste wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position oben im Viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Hauptsteuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der sekundären Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Zum Einrichten einer grauen sekundären Steuerleiste, die 72 Pixel hoch ist und sich am unteren Rand des Viewer-Containers befindet.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
