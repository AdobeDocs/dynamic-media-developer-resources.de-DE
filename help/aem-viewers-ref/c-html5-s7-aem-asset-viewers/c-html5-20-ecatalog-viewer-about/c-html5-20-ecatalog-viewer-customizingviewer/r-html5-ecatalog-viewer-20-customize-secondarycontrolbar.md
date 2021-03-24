---
description: Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen "Erste Seite"und "Letzte Seite"sowie einen Seitenindikator enthält, wenn dieser in CSS verfügbar ist.
solution: Experience Manager
title: Sekundär-Steuerleiste
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Sekundär-Steuerleiste{#secondary-control-bar}

Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen &quot;Erste Seite&quot;und &quot;Letzte Seite&quot;sowie einen Seitenindikator enthält, wenn dieser in CSS verfügbar ist.

Standardmäßig wird sie nur auf Mobiltelefonen angezeigt und befindet sich unten im Viewer. Es benötigt immer die gesamte verfügbare Viewer-Breite. Die Farbe, Höhe und vertikale Position können mit CSS relativ zum Viewer-Container geändert werden.

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
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position oben im Viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Hauptsteuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der sekundären Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer grauen sekundären Steuerleiste, die 72 Pixel hoch und unten im Viewer-Container positioniert ist.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

