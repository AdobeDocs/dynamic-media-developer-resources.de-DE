---
description: 'null'
seo-description: 'null'
seo-title: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
topic: Dynamic media
uuid: b360db52-f705-4966-b77b-009bed729c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zu Zoomaktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird der Einklick-/Tippen-Zoom deaktiviert. Wenn auf <span class="codeph"> Rotationsset </span> eingestellt, wird das Bild in einem Zoomschritt gezoomt. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie auf <span class="codeph"> zurücksetzen </span> klicken, wird der Zoom durch einen einzigen Klick auf das Bild auf die ursprüngliche Rotationsstufe zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird das Zoomen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` auf Desktop-Computern;  `none` auf Touch-Geräten.

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
