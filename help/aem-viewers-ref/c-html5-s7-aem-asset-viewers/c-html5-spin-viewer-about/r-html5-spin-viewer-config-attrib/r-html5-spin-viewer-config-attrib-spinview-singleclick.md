---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick-/Tipp-Zoom-Aktionen. Wenn Sie Keine <span class="codeph"> einstellen</span> wird der Einzelklick/Tippen-Zoom deaktiviert. Wenn diese Option auf <span class="codeph"> eingestellt ist, zoomt </span> Anklicken des Bildes in einem Zoom-Schritt; STRG+Klicken, zoomt in einem Zoom-Schritt heraus. Wenn Sie auf <span class="codeph"> Zurücksetzen setzen setzen </span>, wird mit einem einzigen Klick auf das Bild der Zoom auf den ursprünglichen Drehpegel zurückgesetzt. Für <span class="codeph"> zoomReset-</span> wird Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` Auf Desktop-Computern; `none` auf Touch-Geräten.

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
