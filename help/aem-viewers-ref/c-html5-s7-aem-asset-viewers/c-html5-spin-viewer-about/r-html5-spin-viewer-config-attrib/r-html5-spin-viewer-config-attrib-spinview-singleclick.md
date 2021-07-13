---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic,Viewer,SDK/API,Rotationssets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklicks/Tippen zu Zoom-Aktionen. Wird auf <span class="codeph"> none </span> gesetzt, wird der Zoom durch einfaches Klicken/Tippen deaktiviert. Wenn Sie auf <span class="codeph"> drehen </span> klicken, wird das Bild in einem Zoomschritt vergrößert. Strg+Klicken Zoomt einen Zoomschritt aus. Wird auf <span class="codeph"> </span> zurückgesetzt, wird der Zoom durch einen einzelnen Klick auf das Bild auf die ursprüngliche Rotationsstufe zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet. Andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` auf Desktop-Computern,  `none` auf Touch-Geräten.

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
