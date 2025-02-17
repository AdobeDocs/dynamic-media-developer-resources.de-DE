---
title: Unterstützung für Adobe Analytics-Tracking
description: Der Video-Viewer unterstützt standardmäßig das Tracking von Adobe Analytics.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Der Video-Viewer unterstützt standardmäßig das Tracking von Adobe Analytics.

## Vorkonfiguriertes Tracking {#section-3b101fe30be943c1b679fd5c273569ca}

Der Video-Viewer unterstützt standardmäßig das Tracking von Adobe Analytics.

Um das Tracking zu aktivieren, übergeben Sie den richtigen Namen der Unternehmensvorgabe als `config2`.

Der Viewer sendet außerdem eine einzelne Tracking-HTTP-Anfrage mit den Viewer-Typ- und Versionsinformationen an den konfigurierten Bild-Server.

## Benutzerdefiniertes Tracking {#section-ab10bd7caf184721a366cf3953071934}

Zur Integration mit Analysesystemen von Drittanbietern ist es erforderlich, auf `trackEvent` Viewer-Callback zu lauschen und `eventInfo` Argument der Callback-Funktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

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
   <th colname="col2" class="entry"> <p>Wird gesendet, wenn… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>Der Viewer wird zuerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Ein Asset wird im Viewer mit der API <span class="codeph">setAsset() </span> getauscht. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> MEILENSTEIN </span> </p> </td> 
   <td colname="col2"> <p>Die Wiedergabe erreicht einen der folgenden Meilensteine: 0 %, 25 %, 50 %, 75 % und 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>
