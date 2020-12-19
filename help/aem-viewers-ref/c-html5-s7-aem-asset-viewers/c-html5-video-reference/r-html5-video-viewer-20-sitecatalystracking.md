---
description: Der Video-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.
seo-description: Der Video-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.
seo-title: Unterstützung der Adobe Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Adobe Analytics-Verfolgung
topic: Dynamic media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# Unterstützung für Adobe Analytics-Verfolgung{#support-for-adobe-analytics-tracking}

Der Video-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.

## Vordefinierte Verfolgung {#section-3b101fe30be943c1b679fd5c273569ca}

Der Video-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.

Um die Verfolgung zu aktivieren, übergeben Sie den richtigen Vorgabennamen für die Firma als Parameter `config2`.

Der Viewer sendet außerdem eine einzige Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerspezifische Verfolgung {#section-ab10bd7caf184721a366cf3953071934}

Zur Integration in Analysesysteme von Drittanbietern ist es erforderlich, nach Bedarf auf das `trackEvent`-Viewer-Rückruffunktion zu warten und das `eventInfo`-Argument der Rückruffunktion zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>ein Asset mit der API <span class="codeph"> setAsset() </span> im Viewer getauscht wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>die Wiedergabe gestartet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>Wiedergabe angehalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>Wiedergabe beendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>die Wiedergabe einen der folgenden Meilensteine erreicht: 0%, 25%, 50%, 75% und 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

