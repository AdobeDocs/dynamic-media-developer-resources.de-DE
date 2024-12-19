---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`fade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Anzahl der Sekunden an, die der Spitzentext angezeigt wird, bevor er ausgeblendet wird. Bei <span class="codeph"> -1</span> wird die Meldung immer angezeigt, auch wenn das Flyout aktiviert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Anzahl</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie oft der Text beim Anzeigen neuer Bilder im Set angezeigt wird. Der Wert <span class="codeph"> -1</span> bedeutet, dass der Text immer angezeigt wird, wenn ein Bild im Set angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> verblassen</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer einer Überblendungs -Animation an, die auftritt, wenn der Text angezeigt oder ausgeblendet wird. Ein Wert von <span class="codeph"> 0</span> bedeutet keine Überblendung. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Standard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Beispiel {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
