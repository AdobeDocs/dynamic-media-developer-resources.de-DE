---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic, Viewer, SDK/API, Zoom
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Dublette-Klick/Tippen zu Zoomaktionen. Wenn Sie auf <span class="codeph"> none </span> festlegen, wird der Zoom bei Dublette-Klick/Tippen deaktiviert. Wenn auf <span class="codeph"> </span> festgelegt, klicken Sie in einem Zoomschritt auf das Bild. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie auf <span class="codeph"> zurücksetzen </span> klicken, wird der Zoom durch einen einzigen Klick auf das Bild auf den anfänglichen Zoomgrad zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird das Zoomen angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`reset` auf Desktop-Computern;  `zoomReset` auf Touch-Geräten.

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
