---
description: Unterstützung der Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Analytics-Verfolgung
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 17e8937f-e328-46a4-b7d9-1fd39ab2e8bd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---

# Unterstützung der Analytics-Verfolgung{#support-for-analytics-tracking}

## Benutzerspezifische Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Standardmäßig sendet der Viewer eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

Zur Integration in Analysesysteme von Drittanbietern müssen Sie den `trackEvent`-Viewer-Rückruf abhören und das `eventInfo`-Argument der Rückruffunktion nach Bedarf verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

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
