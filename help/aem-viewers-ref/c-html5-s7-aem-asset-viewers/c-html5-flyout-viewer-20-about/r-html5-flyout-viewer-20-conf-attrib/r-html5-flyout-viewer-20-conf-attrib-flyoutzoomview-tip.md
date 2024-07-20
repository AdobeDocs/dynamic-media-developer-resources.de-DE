---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
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
   <td colname="col2"> <p>Gibt die Anzahl der Sekunden an, nach denen der Tipp-Text angezeigt wird, bevor er ausgeblendet wird. Wenn der Wert auf <span class="codeph"> -1</span> festgelegt ist, wird die Nachricht immer angezeigt, auch wenn der Benutzer den Flyout aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt an, wie oft der Text angezeigt wird, wenn neue Bilder im Set angezeigt werden. Der Wert <span class="codeph"> -1</span> bedeutet, dass der Text immer angezeigt wird, wenn ein Bild im Set angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer einer Überblendung-Animation an, die auftritt, wenn der Text angezeigt oder ausgeblendet wird. Der Wert <span class="codeph"> 0</span> bedeutet, dass keine Überblendung vorhanden ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
