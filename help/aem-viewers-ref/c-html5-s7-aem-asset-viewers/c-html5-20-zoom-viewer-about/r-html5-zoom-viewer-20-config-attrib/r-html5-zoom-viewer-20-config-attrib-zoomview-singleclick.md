---
title: ZoomView.singleClick
description: ZoomView.singleClick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
TQID: 'https://experienceleague.adobe.com/MvEoXp0DRokxvbSt00t8XdgD3dAxEqylyJ2AD6GvJ5g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# ZoomView.singleClick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick-/Tipp-Zoom-Aktionen. Wenn Sie Keine <span class="codeph"> einstellen</span> wird der Einzelklick/Tippen-Zoom deaktiviert. Wenn diese Einstellung aktiviert ist, wird <span class="codeph"> Zoom ausgeführt, </span> durch Klicken auf das Bild in einem Zoom-Schritt ein Bild vergrößert wird; STRG+Klicken verkleinert einen Zoom-Schritt. Wenn Sie auf <span class="codeph"> Zurücksetzen setzen </span>, wird der Zoom mit einem einzigen Klick auf das Bild auf den ursprünglichen Zoomfaktor zurückgesetzt. Für <span class="codeph"> zoomReset-</span> wird Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - Auf Desktop-Computern; `none` auf Touch-Geräten.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
