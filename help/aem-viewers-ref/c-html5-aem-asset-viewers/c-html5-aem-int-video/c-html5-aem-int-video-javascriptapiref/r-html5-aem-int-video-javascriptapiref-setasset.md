---
description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 80c670a4-1251-47f5-a66b-8ba5019df1ce
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# setAsset{#setasset}

JavaScript-API-Referenz für den interaktiven Video-Viewer.

`setAsset(asset[, data])`

Legt das neue Asset und optional zusätzliche Asset-Daten fest. Sie können diesen Parameter jederzeit vor oder nach `init()` aufrufen. Wenn es nach `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} neue Asset-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Daten </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} JSON-Objekt mit den folgenden optionalen Feldern (Groß-/Kleinschreibung beachten): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> posterimage  </span> - Image, das vor dem Abspielen des Beginns im ersten Bild angezeigt wird. Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> caption  </span> - Speicherort der neuen Untertiteldatei. Ist dies nicht der Fall, ist die Beschriftungsschaltfläche in der Benutzeroberfläche nicht sichtbar. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navigation  </span> - URL oder Pfad zum WebVTT-Navigationsinhalt. Die WebVTT-Datei sollte von Image Serving bereitgestellt werden. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData  </span> - URL oder Pfad zu interaktiven WebVTT-Dateninhalten. Die WebVTT-Datei muss von Image Serving bereitgestellt werden. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```

