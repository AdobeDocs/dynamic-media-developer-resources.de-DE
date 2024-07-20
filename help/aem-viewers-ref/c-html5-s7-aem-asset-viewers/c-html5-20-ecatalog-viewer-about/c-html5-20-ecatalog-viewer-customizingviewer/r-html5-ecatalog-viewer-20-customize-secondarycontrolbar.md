---
title: Sekundäre Steuerleiste
description: Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen "Erste und Letzte Seite"und einen Seitenindikator enthält, wenn er in CSS verfügbar gemacht wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Sekundäre Steuerleiste{#secondary-control-bar}

Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen &quot;Erste und Letzte Seite&quot;und einen Seitenindikator enthält, wenn er in CSS verfügbar gemacht wird.

Standardmäßig wird sie nur auf Mobiltelefonen angezeigt und befindet sich unten im Viewer. Es benötigt immer die gesamte verfügbare Viewer-Breite. Es ist möglich, die Farbe, Höhe und vertikale Position durch CSS in Bezug auf den Viewer-Container zu ändern.

Das Erscheinungsbild der sekundären Steuerleiste wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position oben im Viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand des Viewers </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Hauptsteuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der sekundären Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer grauen sekundären Steuerleiste, die 72 Pixel groß und am unteren Rand des Viewer-Containers positioniert ist.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
