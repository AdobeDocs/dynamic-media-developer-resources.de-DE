---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Dublette-Klick/Tippen zu Rotationsaktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird die Dublette-Klick-/Tippen-Rotation deaktiviert. Wenn <span class="codeph"> auf </span> gesetzt, klicken Sie in einem Rotationsschritt auf das Bild. STRG+Klick dreht einen Rotationsschritt aus. Wenn Sie auf <span class="codeph"> zurücksetzen </span> klicken, wird die Rotation durch einen einzigen Klick auf das Bild auf die ursprüngliche Rotation zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Rotationsfaktor auf oder über den angegebenen Grenzwert hinausgeht, andernfalls wird das Drehen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` auf Desktop-Computern;  `zoomReset` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
