---
title: Unterstützung für Adobe Analytics-Tracking
description: Der Video-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Der Video-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.

## Vordefiniertes Tracking {#section-3b101fe30be943c1b679fd5c273569ca}

Der Video-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.

Um das Tracking zu aktivieren, geben Sie den richtigen Unternehmensvorgabennamen als `config2` Parameter.

Der Viewer sendet außerdem eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerdefinierte Verfolgung {#section-ab10bd7caf184721a366cf3953071934}

Zur Integration in Analysesysteme von Drittanbietern ist es erforderlich, `trackEvent` Viewer-Rückruf und -Prozess `eventInfo` -Argument der Callback-Funktion nach Bedarf verwenden. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```javascript {.line-numbers}
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

Der Viewer verfolgt die folgenden SDK-Benutzerereignisse:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK-Benutzerereignis </p> </th> 
   <th colname="col2" class="entry"> <p>Gesendet, wenn ... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>Der Viewer wird zuerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>ein Asset im Viewer mit <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>Die Wiedergabe wird gestartet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>Die Wiedergabe wurde angehalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>Die Wiedergabe wird angehalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>Die Wiedergabe erreicht einen der folgenden Meilensteine: 0 %, 25 %, 50 %, 75 % und 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>
