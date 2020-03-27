---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Dublette-Klick/Tippen zu Rotationsaktionen. Wenn Sie auf <span class="codeph"> "Ohne"einstellen, </span> wird die Rotation bei Dublette-Klick/Tippen deaktiviert. Wenn dies so eingestellt ist, dass beim <span class="codeph"> </span> Klicken auf das Bild in einem Rotationsschritt ein Zoom durchgeführt wird; STRG+Klick dreht einen Rotationsschritt aus. Wenn Sie das <span class="codeph"> Zurücksetzen einstellen, </span> wird die Rotation durch einen einzigen Klick auf das Bild auf die ursprüngliche Rotationsstufe zurückgesetzt. Bei <span class="codeph"> zoomReset </span>wird das Zurücksetzen angewendet, wenn der aktuelle Rotationsfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird das Rotationsverfahren angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`reset` auf Desktop-Computern; auf `zoomReset` Touch-Geräten.

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
