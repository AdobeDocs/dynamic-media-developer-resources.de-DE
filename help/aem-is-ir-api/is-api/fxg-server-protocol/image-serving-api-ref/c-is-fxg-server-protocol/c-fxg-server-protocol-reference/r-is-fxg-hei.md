---
description: Höhe der Ansicht. Gibt die Höhe des Antwortbilds an.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

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

Wenn Sie einen Befehl `scale=1` anwenden, wird eine Rasterformatanforderung in der im FXG angegebenen Größe gerendert.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

Wenn weder `wid=`, `hei=` noch `scale=` angegeben sind, ist das Antwortbild die in der FXG-Ansicht angegebene Standardgröße.

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

