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
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick-/Tipp-Zoom-Aktionen. Wenn Sie Keine <span class="codeph"> einstellen</span> wird der Einzelklick/Tippen-Zoom deaktiviert. Wenn diese Einstellung aktiviert ist, wird <span class="codeph"> Zoom ausgeführt, </span> durch Klicken auf das Bild in einem Zoom-Schritt ein Bild vergrößert wird; STRG+Klicken verkleinert einen Zoom-Schritt. Wenn Sie auf <span class="codeph"> Zurücksetzen setzen </span>, wird der Zoom mit einem einzigen Klick auf das Bild auf den ursprünglichen Zoomfaktor zurückgesetzt. Für <span class="codeph"> zoomReset-</span> wird Zurücksetzen angewendet, wenn der aktuelle Zoomfaktor den angegebenen Grenzwert erreicht oder überschreitet, andernfalls wird Zoom angewendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-edcfcd6c0bd24ac093442c56450b3c97}

Optional.

## Standard {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` auf Desktop-Computern; `none` auf Touch-Geräten.

## Beispiel {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
