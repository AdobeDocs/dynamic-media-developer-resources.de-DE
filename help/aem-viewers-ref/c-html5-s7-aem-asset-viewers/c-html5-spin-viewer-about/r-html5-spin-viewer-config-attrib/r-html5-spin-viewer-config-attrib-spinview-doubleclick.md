---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic, Viewer, SDK/API, Rotationssets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Dublette-Klick/Tippen zu Rotationsaktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird die Dublette-Klick-/Tippen-Rotation deaktiviert. Wenn <span class="codeph"> auf </span> gesetzt, klicken Sie in einem Rotationsschritt auf das Bild. STRG+Klick dreht einen Rotationsschritt aus. Wenn Sie auf <span class="codeph"> zurücksetzen </span> klicken, wird die Rotation durch einen einzigen Klick auf das Bild auf die ursprüngliche Rotation zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Rotationsfaktor auf oder über den angegebenen Grenzwert hinausgeht, andernfalls wird das Drehen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`reset` auf Desktop-Computern;  `zoomReset` auf Touch-Geräten.

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
