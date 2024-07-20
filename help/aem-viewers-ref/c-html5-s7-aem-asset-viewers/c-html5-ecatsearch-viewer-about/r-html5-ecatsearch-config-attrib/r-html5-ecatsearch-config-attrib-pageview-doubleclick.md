---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Doppelklick/Tippen zu Zoom-Aktionen. Wird auf <span class="codeph"> none </span> gesetzt, wird der Doppelklick/Tippen auf Zoom deaktiviert. Wenn der Wert auf <span class="codeph"> Zoom </span> gesetzt ist, wird beim Klicken auf das Bild ein einzoomender Schritt angezeigt. Bei gedrückter Strg-/Klicken-Taste wird ein Zoomschritt verkleinert. Wird auf <span class="codeph"> reset </span> gesetzt, wird der Zoom durch einen einzelnen Klick auf das Bild auf den anfänglichen Zoomfaktor zurückgesetzt. Für <span class="codeph"> zoomReset </span> wird das Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder übersteigt. Andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Optional.

## Standard {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] auf Desktop-Computern; [!DNL `zoomReset`] auf Touch-Geräten.

## Beispiel {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
