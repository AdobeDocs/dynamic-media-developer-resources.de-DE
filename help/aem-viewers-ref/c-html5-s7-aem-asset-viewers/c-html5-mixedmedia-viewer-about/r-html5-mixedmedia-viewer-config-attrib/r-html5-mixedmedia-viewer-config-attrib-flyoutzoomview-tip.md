---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 6%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`verblassen`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Anzahl der Sekunden an, nach denen der Tipp-Text angezeigt wird, bevor er ausgeblendet wird. Wenn auf <span class="codeph"> -1</span>, wird die Nachricht immer angezeigt, auch wenn der Benutzer den Flyout aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft der Text angezeigt wird, wenn neue Bilder im Set angezeigt werden. Ein Wert von <span class="codeph"> -1</span> bedeutet, dass der Text immer angezeigt wird, wenn ein Bild im Set angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> Gibt die Dauer einer Überblendung-Animation an, die auftritt, wenn der Text angezeigt oder ausgeblendet wird. Ein Wert von <span class="codeph"> 0</span> gibt keine Überblendung an. </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
