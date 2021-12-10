---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick/Tippen zu Zoom-Aktionen. Einstellung auf <span class="codeph"> Keine </span> Deaktiviert Doppelklicken/Tippen auf Zoom. Wenn auf <span class="codeph"> Zoom </span> Durch Klicken auf das Bild werden die Zoomschritte in einem Zoomschritt angezeigt. Strg+Klicken Zoomt einen Zoomschritt aus. Einstellung auf <span class="codeph"> reset </span> bewirkt, dass durch einen einzelnen Klick auf das Bild der Zoom auf den anfänglichen Zoomfaktor zurückgesetzt wird. Für <span class="codeph"> zoomReset </span>, wird zurückgesetzt, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`reset` - auf Desktop-Computern, `zoomReset` auf Touch-Geräten.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
