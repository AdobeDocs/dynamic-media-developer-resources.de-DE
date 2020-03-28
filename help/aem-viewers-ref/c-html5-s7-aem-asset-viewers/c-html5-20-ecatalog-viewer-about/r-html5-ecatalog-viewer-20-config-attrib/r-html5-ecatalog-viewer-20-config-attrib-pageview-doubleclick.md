---
description: 'null'
seo-description: 'null'
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: ac4fb532-f554-4831-b341-7f8d6ef3a1c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Dublette-Klick/Tippen zu Zoomaktionen. Wenn Sie auf <span class="codeph"> "Ohne"einstellen, </span> wird der Zoom bei Dublette-Klick/Tippen deaktiviert. Bei Auswahl dieser Option wird das <span class="codeph"> Zoomen durch </span> Klicken auf das Bild in einem Zoomschritt durchgeführt. Strg+Klicken verkleinert einen Zoomschritt. Wenn Sie das <span class="codeph"> Zurücksetzen einstellen, </span> wird der Zoom durch einen einzigen Klick auf das Bild auf den anfänglichen Zoomgrad zurückgesetzt. Bei <span class="codeph"> zoomReset </span>wird der Wert zurückgesetzt, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Optional.

## Standard {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` auf Desktop-Computern; auf `zoomReset` Touch-Geräten.

## Beispiel {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
