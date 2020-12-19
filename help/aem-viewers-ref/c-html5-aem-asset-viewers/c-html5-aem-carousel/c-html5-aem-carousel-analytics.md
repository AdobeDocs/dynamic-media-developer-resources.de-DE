---
description: 'null'
seo-description: 'null'
seo-title: Unterstützung der Adobe Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Adobe Analytics-Verfolgung
topic: Dynamic media
uuid: a7de5549-2a9d-4153-be5e-72705ced85ac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---


# Unterstützung für Adobe Analytics-Verfolgung{#support-for-adobe-analytics-tracking}

## Benutzerspezifische Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Standardmäßig sendet der Viewer eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

Zur Integration in Analysesysteme von Drittanbietern müssen Sie den `trackEvent`-Viewer-Rückruf abhören und das `eventInfo`-Argument der Rückruffunktion nach Bedarf verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> BANNER  </span> </p> </td> 
   <td colname="col2"> <p>das Karussell-Bannerbild geändert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>aktiviert der Benutzer den Hotspot. </p> </td> 
  </tr> 
 </tbody> 
</table>

