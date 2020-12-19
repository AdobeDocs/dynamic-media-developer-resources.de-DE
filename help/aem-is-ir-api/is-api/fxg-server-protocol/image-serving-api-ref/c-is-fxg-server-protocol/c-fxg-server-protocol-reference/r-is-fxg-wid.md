---
description: Breite der Ansicht. Gibt die Breite des Antwortbilds (Ansicht) an.
seo-description: Breite der Ansicht. Gibt die Breite des Antwortbilds (Ansicht) an.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 4%

---


# wid{#wid}

Breite der Ansicht. Gibt die Breite des Antwortbilds (Ansicht) an.

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0), </p></td> 
 </tr> 
</table>

## Standard {#section-830bae0b6bac440098444d7cdcb23e2e}

Wenn weder `wid=`, `hei=` noch `scale=` angegeben sind, ist das Antwortbild die in der FXG-Ansicht angegebene Standardgröße.

Rasterformate werden mit der Einstellung &quot;Standardgröße für Ansichten&quot;(oder &quot;DefaultPix&quot;) gerendert. Klicken Sie auf **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Veröffentlichungseinstellungen]** > **[!UICONTROL Image-Server]** und geben Sie dann die Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Sie müssen Ihre Einstellungen speichern und eine Image Serving-Veröffentlichung durchführen, um eine Änderung anzuwenden.

Wenn Sie einen Befehl `scale=1` anwenden, wird eine Rasterformatanforderung in der im FXG angegebenen Größe gerendert.

## Beispiel {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da die SWF in der Regel bis zur Größe des Browser-Fensters erweitert wird. Daher gelten hei und wid nur für Raster- oder PDF-Formate. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

