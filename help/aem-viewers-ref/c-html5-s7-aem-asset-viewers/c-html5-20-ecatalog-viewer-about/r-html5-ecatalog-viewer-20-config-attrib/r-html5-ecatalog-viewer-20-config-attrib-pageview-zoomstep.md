---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Schritt</span></span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Anzahl der Aktionen zum Ein- und Auszoomen, die erforderlich sind, um die Auflösung um den Faktor zwei zu erhöhen oder zu verringern. Die Auflösungsänderung für jede Zoom-Aktion beträgt 2^1 pro Schritt. Auf <span class="codeph"> 0</span> eingestellt, um mit einer einzigen Zoom-Aktion auf die volle Auflösung zu zoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Limit</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die maximale Zoom-Auflösung relativ zum Bild mit voller Auflösung fest. Der Standardwert ist <span class="codeph"> 1.0</span>, wodurch das Zoomen über die volle Auflösung hinaus nicht möglich ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-636d35a4791447039f1902973f568320}

Optional.

## Standard {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## Beispiel {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
