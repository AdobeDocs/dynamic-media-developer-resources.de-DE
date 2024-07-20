---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Bildvergrößerung für die Flyout-Ansicht relativ zur Hauptansicht an. Muss eine Ganzzahl oder ein Gleitkommawert <span class="codeph"> 1,0</span> oder größer sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Es kann ein optionaler sekundärer Faktor angegeben werden, der durch Klicken oder Tippen auf die Hauptansicht aufgerufen werden kann, wenn die Hervorhebung aktiv ist. Durch Klicken oder Tippen auf ein zweites Mal wird der primäre Zoomfaktor wieder aktiviert. Der Wert <span class="codeph"> -1</span> deaktiviert den sekundären Zoomfaktor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie die Komponente kleine Bilder verarbeitet. </p> <p>Wenn der Wert auf <span class="codeph"> 1</span> festgelegt ist, skaliert die Komponente das Hauptbild so, dass es in die Hauptansicht passt. Außerdem wird das Zoombild so skaliert, dass der konfigurierte Flyout-Fensterbereich vollständig gefüllt ist. </p> <p>Wenn der Wert auf <span class="codeph"> 0</span> gesetzt ist, werden kleine Bilder mit ihrer ursprünglichen Auflösung angezeigt und zentriert im Hauptansichtsbereich und im Flyout-Fenster. Sie können zusätzlichen Leerraum konfigurieren, der um das Bild herum mit einer Hintergrundeigenschaft oder einer ähnlichen CSS-Eigenschaft der CSS-Klassen <span class="codeph"> s7flyoutzoomview</span> und <span class="codeph"> s7flyoutzoom</span> im Hauptansicht- bzw. Flyout-Fenster angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
