---
title: Unterstützung für Adobe Analytics-Tracking
description: Unterstützung für Adobe Analytics-Tracking
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Standardmäßig sendet der Viewer eine einzelne Tracking-HTTP-Anfrage mit den Viewer-Typ- und Versionsinformationen an den konfigurierten Bild-Server.

## Benutzerdefiniertes Tracking {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration mit Analysesystemen von Drittanbietern ist es erforderlich, auf den `trackEvent` Viewer-Callback zu lauschen und das `eventInfo` Argument der Callback-Funktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

Der Viewer verfolgt die folgenden SDK-Benutzerereignisse:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK-Benutzerereignis </p> </th> 
   <th colname="col2" class="entry"> <p>Gesendet… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>Wenn der Viewer zuerst geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>wenn ein Asset im Viewer mit der API <span class="codeph">setAsset() </span> getauscht wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>Wenn die Wiedergabe beginnt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>Wenn die Wiedergabe angehalten wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>Wenn die Wiedergabe gestoppt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MEILENSTEIN </span> </p> </td> 
   <td colname="col2"> <p>Wenn die Wiedergabe einen der folgenden Meilensteine erreicht: 0 %, 25 %, 50 %, 75 % oder 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH-</span> </p> </td> 
   <td colname="col2"> <p>Jedes Mal, wenn der Benutzer auf einen interaktiven Musterabschnitt klickt. </p> </td> 
  </tr> 
 </tbody> 
</table>
