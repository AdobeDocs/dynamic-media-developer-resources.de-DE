---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklicks/Tippen zu Zoom-Aktionen. Einstellung auf <span class="codeph"> Keine </span> Deaktiviert den Zoom durch einfaches Klicken/Tippen. Wenn auf <span class="codeph"> Zoom </span> Durch Klicken auf das Bild werden die Zoomschritte in einem Zoomschritt angezeigt. Strg+Klicken Zoomt einen Zoomschritt aus. Einstellung auf <span class="codeph"> reset </span> bewirkt, dass durch einen einzelnen Klick auf das Bild der Zoom auf den anfänglichen Zoomfaktor zurückgesetzt wird. Für <span class="codeph"> zoomReset </span>, wird zurückgesetzt, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird der Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-edcfcd6c0bd24ac093442c56450b3c97}

Optional.

## Standard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` auf Desktop-Computern, `none` auf Touch-Geräten.

## Beispiel {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
