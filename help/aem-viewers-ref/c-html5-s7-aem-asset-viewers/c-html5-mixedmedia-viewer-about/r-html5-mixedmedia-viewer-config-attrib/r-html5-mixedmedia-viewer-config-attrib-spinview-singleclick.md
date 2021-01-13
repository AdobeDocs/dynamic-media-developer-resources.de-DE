---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
topic: Dynamic media
uuid: 188a4e65-a93e-46c4-89b4-02e745ecf5eb
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zu Zoomaktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird der Einklick-/Tippen-Zoom deaktiviert. Wenn auf <span class="codeph"> </span> festgelegt, klicken Sie in einem Zoomschritt auf das Bild. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie auf <span class="codeph"> zurücksetzen </span> klicken, wird der Zoom durch einen einzigen Klick auf das Bild auf die ursprüngliche Rotationsstufe zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird das Zoomen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` auf Desktop-Computern;  `none` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
