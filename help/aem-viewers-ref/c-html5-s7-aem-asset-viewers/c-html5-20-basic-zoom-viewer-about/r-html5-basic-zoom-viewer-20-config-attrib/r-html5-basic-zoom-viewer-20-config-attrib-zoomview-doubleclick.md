---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Viewer,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick/Tippen zu Zoom-Aktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird der Doppelklick/Tippen auf Zoom deaktiviert. Wenn auf <span class="codeph"> Zoomen </span> festgelegt, wird das Bild durch Klicken in einem Zoomschritt vergrößert. Strg+Klicken Zoomt einen Zoomschritt aus. Wird auf <span class="codeph"> </span> zurückgesetzt, wird der Zoom durch einen einzelnen Klick auf das Bild auf den anfänglichen Zoomfaktor zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet. Andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` auf Desktop-Computern,  `zoomReset` auf Touch-Geräten.

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
