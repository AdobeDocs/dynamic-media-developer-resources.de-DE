---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklicks/Tippen zu Zoom-Aktionen. Wird auf <span class="codeph"> none </span> gesetzt, wird der Zoom durch einmaliges Klicken/Tippen deaktiviert. Wenn der Wert auf <span class="codeph"> Zoom </span> gesetzt ist, wird beim Klicken auf das Bild ein einzoomender Schritt angezeigt. Bei gedrückter Strg-/Klicken-Taste wird ein Zoomschritt verkleinert. Wird auf <span class="codeph"> reset </span> gesetzt, wird der Zoom durch einen einzelnen Klick auf das Bild auf den anfänglichen Zoomfaktor zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder übersteigt. Andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - Auf Desktop-Computern; `none` auf Touch-Geräten.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
