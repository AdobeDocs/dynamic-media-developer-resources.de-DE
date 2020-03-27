---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft. </p> <p>Bei einem Wert von <span class="codeph"> 0 </span>werden keine neuen Bilder während der Größenänderung geladen, und die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Mit der Einstellung <span class="codeph"> 1 </span> können Sie einen oder mehrere BreitenHaltepunkte für das in die Hauptbild-Ansicht geladene Bild angeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haltepunkt, <span class="varname"> Breite </span>[; <span class="varname"> Breite </span></span> </p> </td> 
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
