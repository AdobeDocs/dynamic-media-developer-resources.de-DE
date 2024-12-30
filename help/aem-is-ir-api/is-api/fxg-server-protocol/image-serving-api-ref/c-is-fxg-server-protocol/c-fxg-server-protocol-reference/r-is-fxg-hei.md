---
title: hei
description: Höhe anzeigen. Gibt die Höhe des Antwortbildes an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# hei{#hei}

Höhe anzeigen. Gibt die Höhe des Antwortbildes an.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Val</span></span> </p> </td> 
  <td class="stentry"> <p>Bildhöhe in Pixel (int größer als 0). </p></td> 
 </tr> 
</table>

Rasterformate werden mit der standardmäßigen Ansichtsgröße (oder der Einstellung „DefaultPix„) gerendert. Wählen Sie **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Publish-]** > **[!UICONTROL Bildserver]** aus und geben Sie dann Ihre Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Speichern Sie Ihre Einstellungen und führen Sie eine Image-Serving-Publish durch, um eine Änderung anzuwenden.

Wenn Sie einen `scale=1`-Befehl anwenden, wird eine Rasterformatanforderung in der in der FXG angegebenen Größe gerendert.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

Wenn `wid=`, `hei=` oder `scale=` nicht angegeben sind, entspricht das Antwortbild der standardmäßigen Ansichtsgröße, die in der FXG-Datei angegeben ist.

## Beispiel {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da der SWF normalerweise an die Größe des Browserfensters angepasst wird. Daher gelten hei und wid nur für Raster- oder PDF-Formate. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-Alpha
* PNG-Alpha
