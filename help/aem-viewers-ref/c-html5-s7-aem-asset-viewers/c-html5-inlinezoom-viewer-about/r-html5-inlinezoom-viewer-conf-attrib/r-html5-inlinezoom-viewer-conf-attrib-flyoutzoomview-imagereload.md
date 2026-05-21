---
title: FlyoutZoomView.ImageLoad
description: FlyoutZoomView.ImageLoad
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
TQID: 'https://experienceleague.adobe.com/utzPqD5UMx7TnJK8FvqflzoSjOWGVaGXhKlviY1U9xQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 4%

---

# FlyoutZoomView.ImageLoad{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert, wie die Komponente während der Größenanpassung neue Bilder für die Haupt- und Flyout-Ansicht abruft. </p> <p>Auf <span class="codeph"> </span> 0 festgelegt, lädt die Komponente während der Größenanpassung keine neuen Bilder und die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Mit der Einstellung auf <span class="codeph"> 1 </span> können Sie einen oder mehrere Breitenhaltepunkte für das Bild angeben, das in die Hauptansicht geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breakpoint, <span class="varname"> Breite </span>; <span class="varname"> Breite </span> </span> </p> </td> 
   <td colname="col2"> <p>Breitenhaltepunkte für das Bild, das in die Hauptansicht geladen wird. </p> <p>Die Komponente verwendet immer die beste Einpassgröße für die Erstauslastung. Nach der Größenanpassung wird sichergestellt, dass das Bild in der Hauptansicht immer mit der Breite heruntergeladen wird, die dem nächstgrößeren Breakpoint entspricht, und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
