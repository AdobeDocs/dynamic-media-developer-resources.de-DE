---
title: hei
description: Ansichtshöhe. Gibt die Höhe des Antwortbilds an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# hei{#hei}

Ansichtshöhe. Gibt die Höhe des Antwortbilds an.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildhöhe in Pixel (int größer als 0). </p></td> 
 </tr> 
</table>

Rasterformate werden mit der Einstellung Standardansichtsgröße (oder DefaultPix ) gerendert. Auswählen **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Veröffentlichungseinstellungen]** > **[!UICONTROL Image-Server]** und geben Sie die Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Speichern Sie Ihre Einstellungen und führen Sie eine Image Serving-Veröffentlichung durch, um eine Änderung anzuwenden.

Wenn Sie eine `scale=1` -Befehl, wird eine Rasterformat-Anforderung mit der in der FXG angegebenen Größe gerendert.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

Wenn `wid=`, `hei=`oder `scale=` nicht angegeben sind, ist das Antwortbild die standardmäßige Ansichtsgröße, die in der FXG-Datei angegeben ist.

## Beispiel {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da sich die SWF normalerweise auf die Größe des Browserfensters ausdehnt. Daher gelten hei und wid nur für Raster- oder PDF-Formate. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
