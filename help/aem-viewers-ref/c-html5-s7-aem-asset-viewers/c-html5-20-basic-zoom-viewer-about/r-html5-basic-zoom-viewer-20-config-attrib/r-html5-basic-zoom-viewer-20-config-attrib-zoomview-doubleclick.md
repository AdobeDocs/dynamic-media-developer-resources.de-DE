---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
TQID: 'https://experienceleague.adobe.com/Q68UDbUhC3glR3w6nlXxHFCUlKNbLaNooxP4lcSCBCw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick-/Tipp-Aktionen zum Zoomen. Wenn Sie Keine <span class="codeph"> einstellen, wird </span> Doppelklick/Tippen auf Zoom deaktiviert. Wenn diese Einstellung aktiviert ist, wird <span class="codeph"> Zoom ausgeführt, </span> durch Klicken auf das Bild in einem Zoom-Schritt ein Bild vergrößert wird; STRG+Klicken verkleinert einen Zoom-Schritt. Wenn Sie auf <span class="codeph"> Zurücksetzen setzen </span>, wird der Zoom mit einem einzigen Klick auf das Bild auf den ursprünglichen Zoomfaktor zurückgesetzt. Für <span class="codeph"> zoomReset-</span> wird Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` Auf Desktop-Computern; `zoomReset` auf Touch-Geräten.

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
