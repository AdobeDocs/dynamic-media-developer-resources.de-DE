---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 8dabc31c-ec7e-4dc0-b528-4f3f43f46721
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Dublette-Klick/Tippen zu Zoomaktionen. Wenn Sie auf <span class="codeph"> "Ohne"einstellen, </span> wird der Zoom bei Dublette-Klick/Tippen deaktiviert. Bei Auswahl dieser Option wird das <span class="codeph"> Zoomen durch </span> Klicken auf das Bild in einem Zoomschritt durchgeführt. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie das <span class="codeph"> Zurücksetzen einstellen, </span> wird der Zoom durch einen einzigen Klick auf das Bild auf den anfänglichen Zoomgrad zurückgesetzt. Bei <span class="codeph"> zoomReset </span>wird der Wert zurückgesetzt, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`reset` auf Desktop-Computern; auf `zoomReset` Touch-Geräten.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
