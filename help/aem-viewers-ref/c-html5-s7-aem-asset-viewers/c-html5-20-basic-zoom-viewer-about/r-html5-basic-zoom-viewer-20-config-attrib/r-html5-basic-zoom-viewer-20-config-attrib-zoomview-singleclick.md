---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 42327f03-269b-4d4e-a35d-2537ca3ba071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zu Zoomaktionen. Wenn Sie auf " <span class="codeph"> Ohne"einstellen, </span> wird die Zoom-Funktion durch einmaliges Klicken bzw. Tippen deaktiviert. Bei Auswahl dieser Option wird das <span class="codeph"> Zoomen durch </span> Klicken auf das Bild in einem Zoomschritt durchgeführt. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie das <span class="codeph"> Zurücksetzen einstellen, </span> wird der Zoom durch einen einzigen Klick auf das Bild auf den anfänglichen Zoomgrad zurückgesetzt. Bei <span class="codeph"> zoomReset </span>wird der Wert zurückgesetzt, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` auf Desktop-Computern; auf `none` Touch-Geräten.

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
