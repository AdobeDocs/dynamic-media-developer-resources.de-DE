---
description: Unterstützung der Adobe Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Adobe Analytics-Verfolgung
topic: Dynamic media
uuid: d5399638-3fc5-4f95-841d-5c6d4d35bda2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# Unterstützung für Adobe Analytics-Verfolgung{#support-for-adobe-analytics-tracking}

## Vordefinierte Verfolgung {#section-ba994f079d0343c8ae48adffaa3195a3}

Der Video-Viewer unterstützt standardmäßig die Verfolgung. [!DNL Adobe Analytics] Um die Verfolgung zu aktivieren, übergeben Sie den richtigen Vorgabennamen für die Firma als Parameter `config2`.

Der Viewer sendet außerdem eine einzige Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerspezifische Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration in Analysesysteme von Drittanbietern ist es erforderlich, den `trackEvent` Viewer-Rückruf abzurufen und das `eventInfo`-Argument der Rückruffunktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col2"> <p>ein Asset im Viewer mit der API <span class="codeph"> setAsset() </span> getauscht wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> ein Bild gezoomt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>ein Bild ist geflogen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> ein Bild geändert wird, indem auf ein Farbfeld geklickt oder darauf getippt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

