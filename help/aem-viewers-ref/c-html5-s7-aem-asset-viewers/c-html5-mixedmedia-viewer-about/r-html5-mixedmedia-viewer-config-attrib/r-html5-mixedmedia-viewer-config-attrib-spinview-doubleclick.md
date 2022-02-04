---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick/Tippen zu Rotations-Aktionen. Einstellung auf <span class="codeph"> Keine </span> Deaktiviert Doppelklick/Tippen auf Rotation. Wenn auf <span class="codeph"> Zoom </span>, indem Sie in einem Rotationsschritt auf das Bild klicken; Bei gedrückter Strg-Taste wird ein Rotationsschritt ausgelöst. Einstellung auf <span class="codeph"> reset </span> bewirkt, dass durch einen einzelnen Klick auf das Bild die Rotation auf die ursprüngliche Rotation zurückgesetzt wird. Für <span class="codeph"> zoomReset </span>, wird zurückgesetzt, wenn der aktuelle Rotationsfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird die Rotation angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` auf Desktop-Computern; `zoomReset` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
