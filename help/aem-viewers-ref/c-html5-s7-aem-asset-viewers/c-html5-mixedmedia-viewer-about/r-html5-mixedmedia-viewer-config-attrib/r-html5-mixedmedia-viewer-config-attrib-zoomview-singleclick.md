---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 3e57e235-7888-4ba2-9c8e-4f568a6caa52
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zu Zoomaktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird der Einklick-/Tippen-Zoom deaktiviert. Wenn auf <span class="codeph"> </span> festgelegt, klicken Sie in einem Zoomschritt auf das Bild. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie auf <span class="codeph"> zurücksetzen </span> klicken, wird der Zoom durch einen einzigen Klick auf das Bild auf den anfänglichen Zoomgrad zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird das Zoomen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` auf Desktop-Computern;  `none` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
