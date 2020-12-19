---
description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: e69da809-584c-4311-95c6-3efe9d15ad1f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# getComponent{#getcomponent}

JavaScript-API-Referenz für den interaktiven Video-Viewer.

`getComponent(componentId)`

Gibt einen Verweis auf die Viewer-SDK-Komponente zurück, die vom Viewer verwendet wird. Die Webseite kann diese Methode verwenden, um das Verhalten des standardmäßigen Viewers zu erweitern oder anzupassen. Rufen Sie diese Methode erst nach der Ausführung des Viewer-Rückrufs auf, da die Komponente sonst noch nicht von der Viewer-Logik erstellt wurde.`initComplete`

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` :  `{String}` eine ID der vom Viewer verwendeten Viewer-SDK-Komponente. Dieser Viewer unterstützt die folgenden Komponenten-IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponenten-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Name der Viewer SDK-Komponentenklasse </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Behälter </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoPlayer  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoPlayer  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> interactiveSwatches  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.InteractiveSwatches  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> callToAction  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CallToAction  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeCaptionButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ClosedCaptionButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Steuerelemente </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beim Arbeiten mit SDK-APIs ist es wichtig, den richtigen voll qualifizierten SDK-Namensraum zu verwenden, wie unter [Viewer-SDK-Namensraum](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-html5-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621) beschrieben.

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zur *Viewer SDK API*.

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

`{Object}` eine Referenz zur Viewer-SDK-Komponente. Die Methode gibt `null` zurück, wenn `componentId` keine unterstützte Viewer-Komponente ist oder die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
} 
})
```

