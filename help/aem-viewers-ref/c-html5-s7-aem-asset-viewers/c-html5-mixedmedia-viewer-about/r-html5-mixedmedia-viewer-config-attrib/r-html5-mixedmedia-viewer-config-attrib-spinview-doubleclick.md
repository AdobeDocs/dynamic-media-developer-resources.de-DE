---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick/Tippen zu Rotations-Aktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird das doppelte Klicken/Tippen-Rotieren deaktiviert. Wenn auf <span class="codeph"> Zoomen Sie </span>, indem Sie in einem Rotationsschritt auf die Bilddrehung klicken. Bei gedrückter Strg-Taste wird ein Rotationsschritt ausgelöst. Wenn Sie auf <span class="codeph"> setzen </span>, wird durch einen einzelnen Klick auf das Bild die Rotation auf die ursprüngliche Rotation zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Rotationsfaktor den angegebenen Grenzwert erreicht oder überschreitet. Andernfalls wird die Rotation angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` auf Desktop-Computern,  `zoomReset` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
