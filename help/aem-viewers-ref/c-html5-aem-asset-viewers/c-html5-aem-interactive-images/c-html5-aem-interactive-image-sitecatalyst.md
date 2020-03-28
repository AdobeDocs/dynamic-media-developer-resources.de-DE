---
description: 'null'
seo-description: 'null'
seo-title: Unterstützung der Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Analytics-Verfolgung
topic: Dynamic media
uuid: ae870d2e-2a09-4551-935a-916d0e657653
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterstützung der Analytics-Verfolgung{#support-for-analytics-tracking}

## Benutzerspezifische Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Standardmäßig sendet der Viewer eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

Zur Integration in Analysesysteme von Drittanbietern ist es erforderlich, den `trackEvent` Viewer-Rückruf zu prüfen und das `eventInfo` Argument der Rückruffunktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <th colname="col2" class="entry"> <p>Gesendet, wenn... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>Der Viewer wird zuerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>Benutzer aktiviert Hotspot. </p> </td> 
  </tr> 
 </tbody> 
</table>

