---
description: Der einfache Zoom-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.
seo-description: Der einfache Zoom-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.
seo-title: Unterstützung der Adobe Analytics-Verfolgung
solution: Experience Manager
title: Unterstützung der Adobe Analytics-Verfolgung
topic: Dynamic Media
uuid: f48fde77-7e48-4d56-b5c5-079a484e6d9c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# Unterstützung für Adobe Analytics-Verfolgung{#support-for-adobe-analytics-tracking}

Der einfache Zoom-Viewer unterstützt standardmäßig die Adobe Analytics-Verfolgung.

## Vordefinierte Verfolgung {#section-ba994f079d0343c8ae48adffaa3195a3}

Der einfache Zoom-Viewer unterstützt standardmäßig die Verfolgung. [!DNL Adobe Analytics] Um die Verfolgung zu aktivieren, übergeben Sie den richtigen Vorgabennamen für die Firma als Parameter `config2`.

Der Viewer sendet außerdem eine einzige Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerspezifische Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration in Analysesysteme von Drittanbietern ist es erforderlich, den `trackEvent` Viewer-Rückruf abzurufen und das `eventInfo`-Argument der Rückruffunktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
 </tbody> 
</table>

