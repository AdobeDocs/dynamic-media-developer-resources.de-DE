---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
uuid: 948b154a-250c-41a8-967b-d199ddb6e5e1
feature: Dynamic Media Classic, Viewer, SDK/API, Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> step</span> </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Anzahl der Zoom- und Zoomaktionen, die zum Erhöhen oder Verringern der Auflösung um den Faktor 2 erforderlich sind. Die Auflösungsänderung für jede Zoomaktion beträgt 2^1 pro Schritt. Auf <span class="codeph"> 0</span> setzen, um mit einer einzigen Zoomaktion auf die volle Auflösung zu zoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limit</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die maximale Zoomauflösung relativ zum Bild mit voller Auflösung an. Der Standardwert ist <span class="codeph"> 1.0</span>, was das Zoomen über die vollständige Auflösung hinaus nicht erlaubt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
