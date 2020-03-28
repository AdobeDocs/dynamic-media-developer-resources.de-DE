---
description: Der HTML5-Video360-Viewer unterstützt standardmäßig die Verfolgung durch Adobe Analytics.
seo-description: Der HTML5-Video360-Viewer unterstützt standardmäßig die Verfolgung durch Adobe Analytics.
seo-title: Unterstützung der Adobe Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Adobe Analytics-Verfolgung
topic: Dynamic media
uuid: b5ab903b-3365-45e3-9542-c290c6c42670
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterstützung der Adobe Analytics-Verfolgung{#support-for-adobe-analytics-tracking}

Der HTML5-Video360-Viewer unterstützt standardmäßig die Verfolgung durch Adobe Analytics.

Um die Verfolgung zu aktivieren, übergeben Sie den richtigen Vorgabennamen für die Firma als `config2` Parameter.

Standardmäßig sendet der Viewer eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerspezifische Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration mit Analysesystemen von Drittanbietern ist es erforderlich, den Rückruf des `trackEvent` Viewers abzuhören und das `eventInfo` Argument der Rückruffunktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

Der Viewer verfolgt die folgenden SDK-Ereignis:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK-Ereignis </p> </th> 
   <th colname="col2" class="entry"> <p>Gesendet... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>wenn der Viewer zuerst geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>wenn ein Asset mithilfe der <span class="codeph"> setAsset()- </span> API im Viewer getauscht wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>beim Abspielen von Beginn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>wenn die Wiedergabe angehalten wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>wenn die Wiedergabe beendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>wenn die Wiedergabe einen der folgenden Meilensteine erreicht: 0 %, 25 %, 50 %, 75 % oder 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

