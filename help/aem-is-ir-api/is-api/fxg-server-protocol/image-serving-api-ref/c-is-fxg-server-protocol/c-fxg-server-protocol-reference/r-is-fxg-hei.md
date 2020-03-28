---
description: Höhe der Ansicht. Gibt die Höhe des Antwortbilds an.
seo-description: Höhe der Ansicht. Gibt die Höhe des Antwortbilds an.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

Höhe der Ansicht. Gibt die Höhe des Antwortbilds an.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildhöhe in Pixel (int größer als 0). </p></td> 
 </tr> 
</table>

Rasterformate werden mit der Einstellung &quot;Standardgröße für Ansichten&quot;(oder &quot;DefaultPix&quot;) gerendert. Klicken Sie auf **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Veröffentlichungseinstellungen]** > **[!UICONTROL Image-Server]** und geben Sie dann die Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Sie müssen Ihre Einstellungen speichern und eine Image Serving-Veröffentlichung durchführen, um eine Änderung anzuwenden.

Wenn Sie einen `scale=1` Befehl anwenden, wird eine Rasterformatanforderung in der im FXG angegebenen Größe gerendert.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

Wenn weder `wid=`, `hei=`noch `scale=` angegeben, ist das Antwortbild die in der FXG-Ansicht angegebene Standardgröße.

## Beispiel {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da die SWF in der Regel bis zur Größe des Browser-Fensters erweitert wird. Daher gelten hei und wid nur für Raster- oder PDF-Formate. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

