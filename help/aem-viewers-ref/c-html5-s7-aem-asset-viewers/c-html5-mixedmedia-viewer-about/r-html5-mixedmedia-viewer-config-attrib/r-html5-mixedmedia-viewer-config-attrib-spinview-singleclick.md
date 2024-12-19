---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick-/Tipp-Zoom-Aktionen. Wenn Sie Keine <span class="codeph"> einstellen</span> wird der Einzelklick/Tippen-Zoom deaktiviert. Wenn diese Einstellung aktiviert ist, wird <span class="codeph"> Zoom ausgeführt, </span> durch Klicken auf das Bild in einem Zoom-Schritt ein Bild vergrößert wird; STRG+Klicken verkleinert einen Zoom-Schritt. Wenn Sie auf <span class="codeph"> Zurücksetzen setzen setzen </span>, wird mit einem einzigen Klick auf das Bild der Zoom auf den ursprünglichen Drehpegel zurückgesetzt. Für <span class="codeph"> zoomReset-</span> wird Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` Auf Desktop-Computern; `none` auf Touch-Geräten.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
