---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Bildvergrößerung für die Flyout-Ansicht relativ zur Hauptansicht an. Muss eine Ganzzahl oder ein Gleitkommawert <span class="codeph"> 1,0 </span> oder größer sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Sie können einen optionalen sekundären Faktor angeben, auf den Sie zugreifen können, indem Sie auf die Hauptansicht klicken oder tippen, wenn die Hervorhebung aktiv ist. Durch Klicken oder Tippen auf ein zweites Mal wird zum primären Zoomfaktor zurückgesetzt. Bei einem Wert von <span class="codeph"> -1</span> wird der sekundäre Zoomfaktor deaktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> gehoben</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie die Komponente kleine Bilder verarbeitet. </p> <p>Wenn auf <span class="codeph"> 1 festgelegt</span> skaliert die Komponente das Hauptbild so, dass es in die Hauptansicht passt. Außerdem wird das Zoom-Bild so hochskaliert, dass es den konfigurierten Flyout-Fensterbereich vollständig ausfüllt. </p> <p>Bei <span class="codeph"> 0</span> werden kleine Bilder mit ihrer ursprünglichen Auflösung angezeigt und zentriert im Hauptansichtsbereich und innerhalb des Flyout-Fensters angezeigt. Sie können zusätzlichen Leerraum um das Bild mit einer Background- oder ähnlichen CSS-Eigenschaft der <span class="codeph"> s7flyoutzoomview</span>- und <span class="codeph"> s7flyoutzoom</span>-CSS-Klassen im Hauptansichts- bzw. im Flyout-Fenster konfigurieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
