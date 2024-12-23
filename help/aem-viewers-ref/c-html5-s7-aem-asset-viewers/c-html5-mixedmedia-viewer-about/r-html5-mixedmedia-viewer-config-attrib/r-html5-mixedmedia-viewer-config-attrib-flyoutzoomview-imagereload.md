---
title: FlyoutZoomView.imagereload
description: Konfiguriert, wie die Komponente während der Größenanpassung neue Bilder für die Haupt- und Flyout-Ansicht abruft.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Konfiguriert, wie die Komponente während der Größenanpassung neue Bilder für die Haupt- und Flyout-Ansicht abruft.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Wenn auf <span class="codeph"> 0 </span> festgelegt, lädt die Komponente während der Größenanpassung keine neuen Bilder und die Bildauflösung in der Flyout-Ansicht ändert sich nicht. </p> <p>Bei Einstellung auf <span class="codeph"> 1 können </span> einen oder mehrere Breitenhaltepunkte für das Bild angeben, das in die Hauptansicht geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breakpoint, <span class="varname"> Breite </span>[; <span class="varname"> Breite </span>] </span> </p> </td> 
   <td colname="col2"> <p>Breitenhaltepunkte für das Bild, das in die Hauptansicht geladen wird. Die Komponente verwendet immer die optimale Einpassungsgröße für die Erstauslastung. Nach der Größenanpassung wird sichergestellt, dass das Bild in der Hauptansicht immer mit der Breite heruntergeladen wird, die dem nächstgrößeren Breakpoint entspricht, und auf dem Client herunterskaliert wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
