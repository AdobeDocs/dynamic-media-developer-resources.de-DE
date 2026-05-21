---
title: Unterstützung für Adobe Analytics-Tracking
description: Unterstützung für Adobe Analytics-Tracking
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
TQID: 'https://experienceleague.adobe.com/teYpjABVi1A8dDqyCRf0hCr9RwbIRkWeY7N7OKOHzlM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 0%

---

# Unterstützung für Adobe Analytics-Tracking{#support-for-adobe-analytics-tracking}

## Benutzerdefiniertes Tracking {#section-cda48fc9730142d0bb3326bac7df3271}

Standardmäßig sendet der Viewer eine einzelne Tracking-HTTP-Anfrage mit den Viewer-Typ- und Versionsinformationen an den konfigurierten Bild-Server.

Zur Integration mit Analysesystemen von Drittanbietern ist es erforderlich, auf den `trackEvent` Viewer-Callback zu lauschen und das `eventInfo` Argument der Callback-Funktion nach Bedarf zu verarbeiten.

<!-- The following code is an example of such handler function: -->

<!--

```java {.line-numbers}
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

-->

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
   <td colname="col1"> <p> <span class="codeph"> BANNER </span> </p> </td> 
   <td colname="col2"> <p>Das Bild des Karussellbanners wird geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>Der Benutzer aktiviert den Hotspot. </p> </td> 
  </tr> 
 </tbody> 
</table>
