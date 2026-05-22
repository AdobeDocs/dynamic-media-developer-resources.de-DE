---
title: Unterstützung für Adobe Analytics-Tracking
description: Der Flyout-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: e5ffe8a8-6c25-4fc2-8c25-90bc7e0b416c
TQID: 'https://experienceleague.adobe.com/V1-2H-QPuCMjrirGo8eC-oUE-3KMrmpGSBZZAQuTOXI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 0%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Der Flyout-Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.

## Vorkonfiguriertes Tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

Der Inline-Zoom-Viewer unterstützt standardmäßig [!DNL Adobe Analytics]-Tracking. Um das Tracking zu aktivieren, übergeben Sie den richtigen Namen der Unternehmensvorgabe als `config2`.

Der Viewer sendet außerdem eine einzelne Tracking-HTTP-Anfrage mit den Viewer-Typ- und Versionsinformationen an den konfigurierten Bild-Server.

## Benutzerdefiniertes Tracking {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration mit Analysesystemen von Drittanbietern ist es erforderlich, auf den `trackEvent` Viewer-Callback zu lauschen und das `eventInfo` Argument der Callback-Funktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```javascript {.line-numbers}
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
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>Das Flyout wird aktiviert oder der Zoom-Faktor wird geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p> Ein Bild ist in Planung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FARB-</span> </p> </td> 
   <td colname="col2"> <p> Ein Bild wird durch Klicken oder Tippen auf ein Farbfeld geändert. </p> </td> 
  </tr> 
 </tbody> 
</table>
