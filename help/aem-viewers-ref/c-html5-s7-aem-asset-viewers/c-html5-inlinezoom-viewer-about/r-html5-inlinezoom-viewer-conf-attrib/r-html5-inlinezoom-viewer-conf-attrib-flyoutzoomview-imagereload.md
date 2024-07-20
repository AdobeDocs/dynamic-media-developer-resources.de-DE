---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft. </p> <p>Wird auf <span class="codeph"> 0 </span> gesetzt, lädt die Komponente keine neuen Bilder während der Größenanpassung und die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Mit der Einstellung "<span class="codeph"> 1 </span>" können Sie einen oder mehrere Breitenhaltepunkte für das Bild festlegen, das in die Hauptansicht geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breakpoint, <span class="varname"> Breite </span>; <span class="varname"> Breite </span> </span> </p> </td> 
   <td colname="col2"> <p>Breiten-Haltepunkte für das Bild, das in die Hauptansicht geladen wird. </p> <p>Die Komponente verwendet immer die beste Anpassungsgröße für das anfängliche Laden. Nach der Größenanpassung wird sichergestellt, dass das Bild in der Hauptansicht immer mit der Breite heruntergeladen wird, die dem nächstgrößeren Breakpoint entspricht, und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
