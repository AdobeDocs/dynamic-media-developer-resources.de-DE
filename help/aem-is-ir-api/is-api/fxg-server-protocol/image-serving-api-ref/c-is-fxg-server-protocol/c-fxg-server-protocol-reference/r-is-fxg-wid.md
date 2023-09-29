---
title: wid
description: Anzeigebreite. Gibt die Breite des Antwortbilds (Ansichtsbild) an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# wid{#wid}

Anzeigebreite. Gibt die Breite des Antwortbilds (Ansichtsbild) an.

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0), </p></td> 
 </tr> 
</table>

## Standard {#section-830bae0b6bac440098444d7cdcb23e2e}

Wenn `wid=`, `hei=`, noch `scale=` festgelegt sind, ist das Antwortbild die standardmäßige Ansichtsgröße, die in der FXG-Datei angegeben ist.

Rasterformate werden mit der Einstellung Standardansichtsgröße (oder DefaultPix ) gerendert. Klicks **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Veröffentlichungseinstellungen]** > **[!UICONTROL Image-Server]** und geben Sie die Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Speichern Sie Ihre Einstellungen und führen Sie eine Image Serving-Veröffentlichung durch, um eine Änderung anzuwenden.

Wenn Sie eine `scale=1` -Befehl, wird eine Rasterformat-Anforderung mit der in der FXG angegebenen Größe gerendert.

## Beispiel {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da sich die SWF normalerweise auf die Größe des Browserfensters ausdehnt. Daher `hei` und `wid` nur für Rasterformate oder PDF-Formate. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
