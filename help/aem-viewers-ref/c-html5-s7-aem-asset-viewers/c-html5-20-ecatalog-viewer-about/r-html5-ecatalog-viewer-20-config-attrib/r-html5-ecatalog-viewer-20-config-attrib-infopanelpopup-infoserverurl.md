---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Die URL-Vorlage des Info-Servers wird verwendet, um Schlüssel/Wert-Paare für die Variablenersetzung in der Inhaltsvorlage des Informationsbereichs abzurufen. Die angegebene Vorlage enthält normalerweise Makro-Platzhalter, die durch die tatsächlichen Daten ersetzt werden, bevor die Anfrage an den Server gesendet wird. </p> <p><span class="codeph"> $1$</span> wird durch den Rollover-Wert ersetzt, der die Aktivierung von <span class="codeph"> InfoPanelPopup</span> ausgelöst hat. </p> <p><span class="codeph"> $2$</span> wird durch die Sequenznummer des aktuellen Frames im Bildset ersetzt. </p> <p><span class="codeph"> $3$</span> wird durch das erste Pfadelement ersetzt, das im Namen des übergeordneten Satzes des aktuellen Elements angegeben ist. Dies entspricht normalerweise der Katalog-ID. </p> <p><span class="codeph"> 4$</span> wird durch das folgende Element im Pfad ersetzt und entspricht der Asset-ID. Die eigentliche Syntax der Info-Server-Anfrage ist vom Infoserver abhängig und unterscheidet sich von Server zu Server. Folgendes ist beispielsweise eine typische Dynamic Media Info Server-Anforderungsvorlage: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wenn Sie das Popup für das Infofeld konfigurieren, werden der HTML-Code und der an das Infofeld übergebene JavaScript-Code auf dem Clientcomputer ausgeführt. Stellen Sie daher sicher, dass dieser HTML-Code und JavaScript-Code sicher sind.

## Eigenschaften {#section-71356e3c13244e62b0582980d9d05328}

Optional.

## Standard {#section-22e9af803f724434807d34e200eb7518}

Keine.

## Beispiel {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
