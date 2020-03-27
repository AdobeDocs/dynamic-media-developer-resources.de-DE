---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 7af5e3d3-40c2-4f02-94e2-0314b698905d
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Die URL-Vorlage des Infoservers wird verwendet, um Schlüssel/Wert-Paare für die Variablenersetzung in der Inhaltsvorlage des Infofelds abzurufen. Die angegebene Vorlage enthält in der Regel Makro-Platzhalter, die durch die tatsächlichen Daten ersetzt werden, bevor die Anforderung an den Server gesendet wird. </p> <p><span class="codeph"> $1$</span> wird durch den Rollover-Wert ersetzt, der die <span class="codeph"> InfoPanelPopup</span> -Aktivierung ausgelöst hat. </p> <p><span class="codeph"> $2$</span> wird durch die Sequenznummer des aktuellen Bilds im Bildsatz ersetzt. </p> <p><span class="codeph"> $3$</span> wird durch das erste Pfadelement ersetzt, das im Namen des übergeordneten Satzes des aktuellen Elements angegeben ist. Er entspricht normalerweise der Katalog-ID. </p> <p><span class="codeph"> $4$</span> wird durch das folgende Element im Pfad ersetzt und entspricht der Asset-ID. Die eigentliche Syntax der Infoserver-Anfrage ist vom Infoserver abhängig und unterscheidet sich von Server zu Server. Beispiel: Die folgende Vorlage ist eine typische Scene7-Info-Server-Anforderungsvorlage: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren des Infofeld-Popup der HTML-Code und der an das Infofeld übergebene JavaScript-Code auf dem Client-Computer ausgeführt werden. Stellen Sie daher sicher, dass der HTML-Code und der JavaScript-Code sicher sind.

## Eigenschaften {#section-71356e3c13244e62b0582980d9d05328}

Optional.

## Standard {#section-22e9af803f724434807d34e200eb7518}

Keine.

## Beispiel {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
