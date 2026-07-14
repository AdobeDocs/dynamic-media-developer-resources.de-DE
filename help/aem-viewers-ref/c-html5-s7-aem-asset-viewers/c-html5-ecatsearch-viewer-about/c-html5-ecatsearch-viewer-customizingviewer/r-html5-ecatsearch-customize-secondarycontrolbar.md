---
title: Sekundärer Steuerbalken
description: Die sekundäre Steuerleiste ist der rechteckige Bereich, der die Schaltflächen Erste und Letzte Seite sowie einen Seitenindikator enthält, wenn er in CSS zur Verfügung gestellt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
TQID: 'https://experienceleague.adobe.com/NMaW0QPU2A3pUzpvMg3kbW8MmeLbJ1hZlCSGTEcG6Ko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 171
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

