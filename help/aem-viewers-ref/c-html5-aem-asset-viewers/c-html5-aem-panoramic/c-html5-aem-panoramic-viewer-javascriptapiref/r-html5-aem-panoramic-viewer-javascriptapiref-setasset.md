---
title: setAsset
description: JavaScript-API-Referenz für den Panorama-Viewer.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setAsset{#setasset}

JavaScript-API-Referenz für den Panorama-Viewer.

`setAsset(asset)`

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach der `init()` aufrufen. Wenn es nach dem `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-javascriptapiref/r-html5-aem-panoramic-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} neue Asset-ID. Bilder, die Bild-Rendering (IR) oder benutzergenerierte Inhalte (UGC) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/PanoramicImage-Sample")
```
