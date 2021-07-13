---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic,Viewer,SDK/API,Inline-Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Bildvergrößerung für die Flyout-Ansicht relativ zur Hauptansicht an. Muss ein ganzzahliger oder Gleitkommawert <span class="codeph"> 1.0</span> oder größer sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Es kann ein optionaler sekundärer Faktor angegeben werden, der durch Klicken oder Tippen auf die Hauptansicht aufgerufen werden kann, wenn die Hervorhebung aktiv ist. Durch Klicken oder Tippen auf ein zweites Mal wird der primäre Zoomfaktor wieder aktiviert. Der Wert <span class="codeph"> -1</span> deaktiviert den sekundären Zoomfaktor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie die Komponente kleine Bilder verarbeitet. </p> <p>Wenn auf <span class="codeph"> 1</span> gesetzt, skaliert die Komponente das Hauptbild so, dass es in die Hauptansicht passt. Außerdem wird das Zoombild so skaliert, dass der konfigurierte Flyout-Fensterbereich vollständig gefüllt ist. </p> <p>Wenn auf <span class="codeph"> 0</span> gesetzt, werden kleine Bilder mit ihrer ursprünglichen Auflösung angezeigt und zentriert im Hauptansichtsbereich und innerhalb des Flyout-Fensters. Sie können den zusätzlichen Leerraum um das Bild herum mit einer Hintergrundeigenschaft oder einer ähnlichen CSS-Eigenschaft der CSS-Klassen <span class="codeph"> s7flyoutzoomview</span> und <span class="codeph"> s7flyoutzoom</span> CSS in der Hauptansicht bzw. im Flyout-Fenster konfigurieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
