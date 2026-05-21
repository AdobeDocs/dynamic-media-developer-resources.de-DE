---
title: hei
description: Höhe anzeigen. Gibt die Höhe des Antwortbildes an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
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

Rasterformate werden mit der standardmäßigen Ansichtsgröße (oder der Einstellung „DefaultPix„) gerendert. Wählen Sie **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Veröffentlichungseinrichtung]** > **[!UICONTROL Image-Server]** aus und geben Sie dann Ihre Werte für Breite und Höhe ein. Kleinere Größen bieten eine bessere Leistung. Speichern Sie Ihre Einstellungen und führen Sie eine Image-Serving-Veröffentlichung durch, um eine Änderung anzuwenden.

Wenn Sie einen `scale=1`-Befehl anwenden, wird eine Rasterformatanforderung in der in der FXG angegebenen Größe gerendert.

## Standard {#section-76ee3daa77cb468ab310821357cc9404}

Wenn `wid=`, `hei=` oder `scale=` nicht angegeben sind, entspricht das Antwortbild der standardmäßigen Ansichtsgröße, die in der FXG-Datei angegeben ist.

## Beispiel {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Sofern kein Format angegeben ist, wird das Bild als SWF-Datei gerendert. In diesem Fall haben Höhe und Breite keine Bedeutung, da der SWF normalerweise an die Größe des Browserfensters angepasst wird. Daher gelten hei und wid nur für Rasterformate oder PDF. Zu den Rasterformaten gehören:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-Alpha
* TIF-Alpha
* PNG-Alpha
