---
title: getComponent
description: JavaScript-API-Referenz für Viewer für gemischte Medien
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0dc6ad78-1044-4495-9414-53900302b8c0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# getComponent{#getcomponent}

JavaScript-API-Referenz für Viewer für gemischte Medien

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
   <td colname="col1"> <p> <span class="codeph"> zoomView-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> flyoutZoomView-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SpinView-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoPlayer-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoPlayer-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar-</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> closedCaptionButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ClosedCaptionButton-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Farbfelder </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.swatches-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colorSwatches-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.swatches-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinLeftButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinRightButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton-</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton-</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton-</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bei der Arbeit mit SDK-APIs ist es wichtig, den richtigen und vollständig qualifizierten SDK-Namespace zu verwenden, wie in [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) beschrieben.

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zur Viewer-SDK-API .

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-SDK-Komponente. Die Methode gibt `null` zurück, wenn die `componentId` keine unterstützte Viewer-Komponente ist oder wenn die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```

```
