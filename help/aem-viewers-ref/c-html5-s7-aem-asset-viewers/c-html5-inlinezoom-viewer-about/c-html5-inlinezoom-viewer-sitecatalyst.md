---
title: Unterstützung für Adobe Analytics-Tracking
description: Der Flyout-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: e5ffe8a8-6c25-4fc2-8c25-90bc7e0b416c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Der Flyout-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.

## Vordefiniertes Tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

Der Inline-Zoom-Viewer unterstützt [!DNL Adobe Analytics] standardmäßiges Tracking. Um das Tracking zu aktivieren, geben Sie den richtigen Unternehmensvorgabennamen als `config2` Parameter.

Der Viewer sendet außerdem eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerdefinierte Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration in Analysesysteme von Drittanbietern ist es erforderlich, die `trackEvent` Viewer-Rückruf und Verarbeitung der `eventInfo` -Argument der Callback-Funktion nach Bedarf verwenden. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
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
   <td colname="col2"> <p>der Viewer zuerst geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>ein Asset im Viewer mit <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>der Flyout aktiviert oder der Zoomfaktor geändert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p> ein Bild eingeplant ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> ein Bild geändert wird, indem Sie auf ein Muster klicken oder tippen. </p> </td> 
  </tr> 
 </tbody> 
</table>
