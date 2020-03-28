---
description: 'null'
seo-description: 'null'
seo-title: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
topic: Dynamic media
uuid: 188a4e65-a93e-46c4-89b4-02e745ecf5eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zu Zoomaktionen. Wenn Sie auf " <span class="codeph"> Ohne"einstellen, </span> wird die Zoom-Funktion durch einmaliges Klicken bzw. Tippen deaktiviert. Bei Auswahl dieser Option wird das <span class="codeph"> Zoomen durch </span> Klicken auf das Bild in einem Zoomschritt durchgeführt. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie das <span class="codeph"> Zurücksetzen einstellen, </span> wird der Zoom durch einen einzigen Klick auf das Bild auf den anfänglichen Rotationspegel zurückgesetzt. Bei <span class="codeph"> zoomReset </span>wird der Wert zurückgesetzt, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` auf Desktop-Computern; auf `none` Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
