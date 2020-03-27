---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: 16a0ca99-1ed5-4f1d-b068-55adc46fde0b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durationcountfade`*[, *``*][, *``*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie viele Sekunden der Tipp-Text angezeigt wird, bevor er ausgeblendet wird. Bei Festlegung auf <span class="codeph"> -1</span>wird die Meldung immer angezeigt, auch wenn der Benutzer den Flyout aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft der Text angezeigt wird, wenn neue Bilder im Satz angezeigt werden. Der Wert <span class="codeph"> -1</span> bedeutet, dass der Text immer angezeigt wird, wenn ein Bild im Satz angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> Gibt die Dauer einer Überblendungsanimation an, die eintritt, wenn der Text angezeigt oder ausgeblendet wird. Der Wert <span class="codeph"> 0</span> bedeutet, dass keine Transition ausgeblendet wird. </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
