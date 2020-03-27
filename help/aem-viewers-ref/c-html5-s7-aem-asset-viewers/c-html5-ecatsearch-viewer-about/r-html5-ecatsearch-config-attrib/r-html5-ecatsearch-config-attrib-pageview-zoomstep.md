---
description: 'null'
seo-description: 'null'
seo-title: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
topic: Dynamic media
uuid: 27eb2a48-008b-455e-9a03-41bb4030271b
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *``*[, *`steplimit`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Schritt</span></span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Anzahl der Zoom- und Zoomaktionen, die zum Erhöhen oder Verringern der Auflösung um den Faktor 2 erforderlich sind. Die Auflösungsänderung für jede Zoomaktion beträgt 2^1 pro Schritt. Auf <span class="codeph"> 0</span> setzen, um mit einer einzigen Zoomaktion auf die volle Auflösung zu zoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Grenze</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die maximale Zoomauflösung relativ zum Bild mit voller Auflösung an. Der Standardwert ist <span class="codeph"> 1,0</span>, was das Zoomen über die volle Auflösung hinaus nicht erlaubt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-636d35a4791447039f1902973f568320}

Optional.

## Standard {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Beispiel {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
