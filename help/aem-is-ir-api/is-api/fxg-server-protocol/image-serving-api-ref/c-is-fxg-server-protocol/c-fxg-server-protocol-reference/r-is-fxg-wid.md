---
title: WID
description: Breite anzeigen. Gibt die Breite des Antwortbildes (Ansichtsbild) an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# WID{#wid}

Breite anzeigen. Gibt die Breite des Antwortbildes (Ansichtsbild) an.

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0), </p></td> 
 </tr> 
</table>

## Standard {#section-830bae0b6bac440098444d7cdcb23e2e}

Wenn weder `wid=`, `hei=` noch `scale=` angegeben sind, entspricht das Antwortbild der standardmäßigen Ansichtsgröße, die in der FXG-Datei angegeben ist.

Rasterformate werden mit der standardmäßigen Ansichtsgröße (oder der Einstellung „DefaultPix„) gerendert. Klicken Sie auf **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Veröffentlichungseinstellungen]** > **[!UICONTROL Image-Server]** und geben Sie dann Ihre Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Speichern Sie Ihre Einstellungen und führen Sie eine Image-Serving-Veröffentlichung durch, um eine Änderung anzuwenden.

Wenn Sie einen `scale=1`-Befehl anwenden, wird eine Rasterformatanforderung in der in der FXG angegebenen Größe gerendert.

## Beispiel {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da der SWF normalerweise an die Größe des Browserfensters angepasst wird. Daher gelten `hei` und `wid` nur für Raster- oder PDF-Formate. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-Alpha
* TIF-Alpha
* PNG-Alpha
