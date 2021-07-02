---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Schritt</span></span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Anzahl der Vergrößerungs- und Verkleinerungsaktionen, die zum Vergrößern oder Verkleinern der Auflösung um den Faktor zwei erforderlich sind. Die Auflösung für jede Zoom-Aktion beträgt 2^1 pro Schritt. Auf <span class="codeph"> 0</span> setzen, um mit einer einzigen Zoom-Aktion auf die vollständige Auflösung zu zoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Grenze</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die maximale Zoomauflösung relativ zum Bild mit voller Auflösung an. Der Standardwert ist <span class="codeph"> 1.0</span>, was das Zoomen über die vollständige Auflösung hinaus nicht erlaubt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
