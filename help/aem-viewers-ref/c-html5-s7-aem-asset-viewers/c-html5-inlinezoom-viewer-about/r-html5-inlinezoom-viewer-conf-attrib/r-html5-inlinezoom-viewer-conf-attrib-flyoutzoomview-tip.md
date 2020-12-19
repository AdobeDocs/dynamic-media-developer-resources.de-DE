---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: 42bbef39-36b6-4f1d-a228-0aaf107600a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 6%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durationcountfade `*[, *``*][, *``*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie viele Sekunden der Tipp-Text angezeigt wird, bevor er ausgeblendet wird. Bei Festlegung auf <span class="codeph"> -1</span> wird die Meldung immer angezeigt, auch wenn der Benutzer das Flyout aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie oft der Text angezeigt wird, wenn neue Bilder im Satz angezeigt werden. Der Wert <span class="codeph"> -1</span> bedeutet, dass der Text immer angezeigt wird, wenn ein Bild im Satz angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> verblassen</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer einer Überblendungsanimation an, die eintritt, wenn der Text angezeigt oder ausgeblendet wird. Der Wert <span class="codeph"> 0</span> bedeutet, dass keine Transition ausgeblendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
