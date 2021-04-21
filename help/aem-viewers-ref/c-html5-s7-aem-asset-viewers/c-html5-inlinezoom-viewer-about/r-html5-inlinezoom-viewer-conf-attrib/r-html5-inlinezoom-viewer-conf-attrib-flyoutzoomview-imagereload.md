---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft. </p> <p>Bei Festlegung auf <span class="codeph"> 0 </span> lädt die Komponente keine neuen Bilder während der Größenänderung und die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Bei Festlegung auf <span class="codeph"> 1 </span> können Sie einen oder mehrere BreitenHaltepunkte für das Bild angeben, das in die Haupt-Ansicht geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haltepunkt,  <span class="varname"> Breite  </span>;  <span class="varname"> width  </span> </span> </p> </td> 
   <td colname="col2"> <p>Breiten-Haltepunkte für das Bild, das in die Haupt-Ansicht geladen wird. </p> <p>Die Komponente verwendet immer die für die anfängliche Belastung am besten geeignete Größe. Nach dem Ändern der Größe wird sichergestellt, dass das Bild in der Haupt-Ansicht immer mit der Breite heruntergeladen wird, die dem nächstgrößeren Haltepunkt entspricht, und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
