---
description: Der eCatalog Search Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.
solution: Experience Manager
title: Unterstützung für Adobe Analytics-Tracking
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

Der eCatalog Search Viewer unterstützt standardmäßig das Adobe Analytics-Tracking.

## Vordefiniertes Tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

Der eCatalog Search Viewer unterstützt standardmäßig das [!DNL Adobe Analytics]-Tracking. Um das Tracking zu aktivieren, übergeben Sie den richtigen Unternehmensvorgabennamen als Parameter `config2` .

Der Viewer sendet außerdem eine einzelne Tracking-HTTP-Anforderung mit dem Viewer-Typ und den Versionsinformationen an den konfigurierten Image-Server.

## Benutzerdefinierte Verfolgung {#section-cda48fc9730142d0bb3326bac7df3271}

Zur Integration in Analytics-Systeme von Drittanbietern ist es erforderlich, den `trackEvent` Viewer-Rückruf zu überwachen und das `eventInfo` -Argument der Callback-Funktion nach Bedarf zu verarbeiten. Der folgende Code ist ein Beispiel für eine solche Handler-Funktion:

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
   <td colname="col2"> <p>ein Asset im Viewer mithilfe der API <span class="codeph"> setAsset() </span> ausgetauscht wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> ein Bild gezoomt wird. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> SEITE </span> </p> </td> 
   <td colname="col2"> <p> wird ein aktueller Frame in der Hauptansicht geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ELEMENT </span> </p> </td> 
   <td colname="col2"> <p>Ein Popup für das Informationsfeld wird aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>ein Benutzer zu einer anderen Seite navigiert, weil er auf die Imagemap klickt. </p> </td> 
  </tr> 
 </tbody> 
</table>
