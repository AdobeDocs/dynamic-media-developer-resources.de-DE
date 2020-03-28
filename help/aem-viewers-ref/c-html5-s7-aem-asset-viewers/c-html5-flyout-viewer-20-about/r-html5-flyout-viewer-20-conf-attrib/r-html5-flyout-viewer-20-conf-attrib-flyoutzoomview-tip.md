---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: ad423dc7-4dd8-42d9-bf75-db8f309f6aaa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durationcountfade`*[, *``*][, *``*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie viele Sekunden der Tipp-Text angezeigt wird, bevor er ausgeblendet wird. Bei Festlegung auf <span class="codeph"> -1</span>wird die Meldung immer angezeigt, auch wenn der Benutzer den Flyout aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Anzahl</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie oft der Text angezeigt wird, wenn neue Bilder im Satz angezeigt werden. Der Wert <span class="codeph"> -1</span> bedeutet, dass der Text immer angezeigt wird, wenn ein Bild im Satz angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer einer Überblendungsanimation an, die eintritt, wenn der Text angezeigt oder ausgeblendet wird. Der Wert <span class="codeph"> 0</span> bedeutet keine Transition der Überblendung. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
