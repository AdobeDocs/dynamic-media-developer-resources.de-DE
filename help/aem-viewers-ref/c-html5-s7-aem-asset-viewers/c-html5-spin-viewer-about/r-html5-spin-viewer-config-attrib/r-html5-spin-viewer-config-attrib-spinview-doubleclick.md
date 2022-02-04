---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick/Tippen zu Rotations-Aktionen. Einstellung auf <span class="codeph"> Keine </span> Deaktiviert Doppelklick/Tippen auf Rotation. Wenn auf <span class="codeph"> Zoom </span>, indem Sie in einem Rotationsschritt auf das Bild klicken; Bei gedrückter Strg-Taste wird ein Rotationsschritt ausgelöst. Einstellung auf <span class="codeph"> reset </span> bewirkt, dass durch einen einzelnen Klick auf das Bild die Rotation auf die ursprüngliche Rotation zurückgesetzt wird. Für <span class="codeph"> zoomReset </span>, wird zurückgesetzt, wenn der aktuelle Rotationsfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird die Rotation angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`reset` auf Desktop-Computern, `zoomReset` auf Touch-Geräten.

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
