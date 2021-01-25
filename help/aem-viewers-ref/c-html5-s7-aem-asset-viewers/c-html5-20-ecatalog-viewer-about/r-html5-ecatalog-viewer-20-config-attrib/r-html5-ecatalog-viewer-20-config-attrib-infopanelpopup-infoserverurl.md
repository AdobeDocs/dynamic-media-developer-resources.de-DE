---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Die URL-Vorlage des Infoservers wird verwendet, um Schlüssel/Wert-Paare für die Variablenersetzung in der Inhaltsvorlage des Infofelds abzurufen. Die angegebene Vorlage enthält in der Regel Makro-Platzhalter, die durch die tatsächlichen Daten ersetzt werden, bevor die Anforderung an den Server gesendet wird. </p> <p><span class="codeph"> $1$</span> wird durch den Rollover-Wert ersetzt, der die  <span class="codeph"> </span> InfoPanelPopupaktivierung auslöste. </p> <p><span class="codeph"> $2$</span> wird durch die Sequenznummer des aktuellen Bilds im Bildsatz ersetzt. </p> <p><span class="codeph"> $3$</span> wird durch das erste Pfadelement ersetzt, das im Namen des übergeordneten Satzes des aktuellen Elements angegeben ist. Er entspricht normalerweise der Katalog-ID. </p> <p><span class="codeph"> $4$</span> wird durch das folgende Element im Pfad ersetzt und entspricht der Asset-ID. Die eigentliche Syntax der Infoserver-Anfrage ist vom Infoserver abhängig und unterscheidet sich von Server zu Server. Beispiel: Die folgende Vorlage ist eine typische Dynamic Media Info-Server-Anforderungsvorlage: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
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

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
