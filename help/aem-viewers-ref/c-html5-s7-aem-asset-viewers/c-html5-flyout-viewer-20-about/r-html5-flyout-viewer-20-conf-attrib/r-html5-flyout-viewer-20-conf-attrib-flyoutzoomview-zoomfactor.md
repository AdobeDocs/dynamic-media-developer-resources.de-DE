---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
TQID: 'https://experienceleague.adobe.com/Zp4VYoGBfivwXRZQ7dmtouoy2qFMZePQKDrocHaBPXk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
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
   <td colname="col2"> <p>Gibt an, wie die Komponente kleine Bilder verarbeitet. </p> <p>Wenn auf <span class="codeph"> 1 festgelegt</span> skaliert die Komponente das Hauptbild so, dass es in die Hauptansicht passt. Außerdem wird das Zoom-Bild so hochskaliert, dass es den konfigurierten Flyout-Fensterbereich vollständig ausfüllt. </p> <p>Bei <span class="codeph"> 0</span> werden kleine Bilder mit ihrer ursprünglichen Auflösung angezeigt und zentriert im Hauptansichtsbereich und innerhalb des Flyout-Fensters angezeigt. Sie können zusätzlichen Leerraum konfigurieren, der um das Bild mit einer Hintergrund- oder ähnlichen CSS-Eigenschaft der <span class="codeph"> s7flyoutzoomview</span>- und <span class="codeph"> s7flyoutzoom</span>-CSS-Klassen im Hauptansichts- bzw. Flyout-Fenster angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
