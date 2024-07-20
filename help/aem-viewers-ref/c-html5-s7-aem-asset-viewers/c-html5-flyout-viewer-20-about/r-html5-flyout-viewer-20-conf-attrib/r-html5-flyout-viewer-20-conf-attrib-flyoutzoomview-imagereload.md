---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert, wie die Komponente neue Bilder für die Haupt- und Flyout-Ansicht während der Größenanpassung abruft. </p> <p>Wenn der Wert auf <span class="codeph"> 0 </span> festgelegt ist, lädt die Komponente keine neuen Bilder während der Größenanpassung. Die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Wenn Sie auf <span class="codeph"> 1 </span> festlegen, können Sie einen oder mehrere Breitenhaltepunkte für das Bild festlegen, das in die Hauptansicht geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breakpoint, <span class="varname"> Breite </span>[; <span class="varname"> Breite </span>] </span> </p> </td> 
   <td colname="col2"> <p> Breiten-Haltepunkte für das Bild, das in die Hauptansicht geladen wird. Die Komponente verwendet immer die beste Anpassungsgröße für das anfängliche Laden. Nach der Größenanpassung wird sichergestellt, dass das Bild in der Hauptansicht immer mit der Breite heruntergeladen wird, die dem nächstgrößeren Breakpoint entspricht, und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
