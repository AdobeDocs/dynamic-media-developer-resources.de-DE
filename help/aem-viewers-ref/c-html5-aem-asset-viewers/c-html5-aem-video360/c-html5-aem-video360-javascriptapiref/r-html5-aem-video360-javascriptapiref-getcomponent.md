---
title: getComponent
description: JavaScript-API-Referenz für Video360-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: bc5f0046-8e20-4ff0-a90f-05c38f686ad2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# getComponent{#getcomponent}

JavaScript-API-Referenz für Video360-Viewer.

`getComponent(componentId)`

Gibt einen Verweis auf die Viewer-SDK-Komponente zurück, die vom Viewer verwendet wird. Die Web-Seite kann diese Methode verwenden, um das Verhalten des vordefinierten Viewers zu erweitern oder anzupassen. Rufen Sie diese Methode erst auf, nachdem der `initComplete` Viewer-Rückruf ausgeführt wurde. Andernfalls wird die Komponente möglicherweise noch nicht von der Viewer-Logik erstellt.

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` eine ID der Viewer-SDK-Komponente an, die vom Viewer verwendet wird. Dieser Viewer unterstützt die folgenden Komponenten-IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponenten-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Name der Viewer-SDK-Komponentenklasse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> MediaSet-</span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> video360player </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.video360Player </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> veränderlicher </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sk.share.EmbedShare </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bei der Arbeit mit SDK-APIs ist es wichtig, den richtigen, vollständig qualifizierten SDK-Namespace zu verwenden, wie in [Viewer-SDK-Namespace](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621) beschrieben.

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zur *-Viewer-SDK-API für* HTML5&rbrace;.

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Die `{Object}` ist ein Verweis auf die Viewer-SDK-Komponente. Die Methode gibt `null` zurück, wenn die `componentId` keine unterstützte Viewer-Komponente ist oder wenn die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var video360Player = <instance>.getComponent("video360Player"); 
} 
})
```
