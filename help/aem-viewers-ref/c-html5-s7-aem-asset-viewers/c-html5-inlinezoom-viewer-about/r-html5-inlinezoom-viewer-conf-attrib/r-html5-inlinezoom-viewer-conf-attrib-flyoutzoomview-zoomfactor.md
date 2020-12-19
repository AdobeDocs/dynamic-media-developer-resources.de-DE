---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Bildvergrößerung für die Flyout-Ansicht relativ zur Haupt-Ansicht an. Muss eine Ganzzahl oder ein Gleitkommawert <span class="codeph"> 1.0</span> oder größer sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Es kann ein optionaler sekundärer Faktor angegeben werden, auf den zugegriffen werden kann, indem auf die Haupt-Ansicht geklickt oder getippt wird, wenn die Hervorhebung aktiv ist. Durch Klicken oder Tippen auf ein zweites Mal wird der primäre Zoomfaktor wiederhergestellt. Der Wert <span class="codeph"> -1</span> deaktiviert den sekundären Zoomfaktor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie die Komponente mit kleinen Bildern umgeht. </p> <p>Wenn die Komponente auf <span class="codeph"> 1</span> eingestellt ist, wird das Hauptbild so skaliert, dass es in die Haupt-Ansicht passt. Außerdem wird das Zoombild so skaliert, dass der konfigurierte Flyout-Fensterbereich vollständig gefüllt wird. </p> <p>Wenn auf <span class="codeph"> 0</span> eingestellt, werden kleine Ansichten mit der Originalauflösung angezeigt und zentriert im Hauptbereich und im Flyout-Fenster angezeigt. Sie können zusätzliche Leerräume um das Bild mit einer Hintergrund- oder ähnlichen CSS-Eigenschaft der CSS-Klassen <span class="codeph"> s7flyoutzoomview</span> und <span class="codeph"> s7flyoutzoom</span> im Haupt- bzw. Flyout-Ansicht konfigurieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
