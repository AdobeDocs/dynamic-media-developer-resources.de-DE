---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`width`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft. </p> <p>Bei Festlegung auf <span class="codeph"> 0 </span> lädt die Komponente keine neuen Bilder während der Größenanpassung. Die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Wenn Sie auf <span class="codeph"> 1 </span> festlegen, können Sie einen oder mehrere BreitenHaltepunkte für das in die Hauptbild geladene Ansicht angeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haltepunkt,  <span class="varname"> Breite  </span>[;  <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> Breiten-Haltepunkte für das Bild, das in die Haupt-Ansicht geladen wird. Die Komponente verwendet immer die für die anfängliche Belastung am besten geeignete Größe. Nach der Größenanpassung wird sichergestellt, dass das Bild in der Haupt-Ansicht immer mit der Breite des nächstgrößeren Haltepunkts heruntergeladen und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
