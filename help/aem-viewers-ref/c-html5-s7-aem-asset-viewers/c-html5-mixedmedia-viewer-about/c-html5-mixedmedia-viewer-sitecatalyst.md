---
description: Der Viewer für gemischte Medien unterstützt standardmäßig das Adobe Analytics-Tracking.
solution: Experience Manager
title: Unterstützung für Adobe Analytics-Tracking
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 3b28c853-3747-4805-a141-3cce1398d783
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 5%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Der Viewer für gemischte Medien unterstützt standardmäßig das Adobe Analytics-Tracking.

## Vordefiniertes Tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

Der Viewer für gemischte Medien unterstützt die standardmäßige [!DNL Adobe Analytics]-Verfolgung. Um das Tracking zu aktivieren, übergeben Sie den richtigen Unternehmensvorgabennamen als Parameter `config2` .

Der Viewer sendet außerdem eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerdefinierte Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Um in Analytics-Systeme von Drittanbietern zu integrieren, müssen Sie den Viewer-Rückruf `trackEvent` überwachen und das `eventInfo`-Argument der Callback-Funktion nach Bedarf verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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
   <td colname="col2"> <p>Ein Asset wird im Viewer mithilfe der API <span class="codeph"> setAsset() </span> ausgetauscht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>ein Bild gezoomt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>ein Bild eingeplant ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> ein Bild geändert wird, indem Sie auf ein Muster klicken oder tippen. </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p>drehen wird. </p> </td> 
  </tr> 
 </tbody> 
</table>
