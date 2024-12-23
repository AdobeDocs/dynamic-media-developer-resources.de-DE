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
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick-/Tipp-Aktionen, um Aktionen zu drehen. Wenn Sie Keine <span class="codeph"> festlegen, wird </span> Doppelklick-/Tippen-Drehen deaktiviert. Wenn <span class="codeph"> Zoom-</span> festgelegt ist, wird beim Klicken auf das Bild in einem Rotationsschritt gedreht. Bei gedrückter Strg-Taste wird ein Rotationsschritt ausgegeben. Wenn Sie auf <span class="codeph"> Zurücksetzen setzen setzen </span>, wird mit einem einzigen Klick auf das Bild der ursprüngliche Drehpegel zurückgesetzt. Für <span class="codeph"> zoomReset-</span> wird das Zurücksetzen angewendet, wenn der aktuelle Rotationsfaktor den angegebenen Grenzwert erreicht oder überschreitet. Andernfalls wird das Drehen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Auf Desktop-Computern; `zoomReset` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
