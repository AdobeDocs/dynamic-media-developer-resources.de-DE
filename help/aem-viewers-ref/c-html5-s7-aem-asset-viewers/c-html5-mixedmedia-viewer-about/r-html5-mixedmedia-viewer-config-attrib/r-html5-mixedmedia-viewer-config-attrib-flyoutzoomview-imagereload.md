---
description: Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft.
seo-description: Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft.
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Bei Festlegung auf <span class="codeph"> 0 </span> lädt die Komponente keine neuen Bilder während der Größenänderung und die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Bei Festlegung auf <span class="codeph"> 1 </span> können Sie einen oder mehrere BreitenHaltepunkte für das Bild angeben, das in die Haupt-Ansicht geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haltepunkt,  <span class="varname"> Breite  </span>[;  <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>Breiten-Haltepunkte für das Bild, das in die Haupt-Ansicht geladen wird. Die Komponente verwendet immer die beste passende Größe für die anfängliche Belastung. Nach dem Ändern der Größe wird sichergestellt, dass das Bild in der Haupt-Ansicht immer mit einer Breite heruntergeladen wird, die dem nächstgrößeren Haltepunkt entspricht, und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
