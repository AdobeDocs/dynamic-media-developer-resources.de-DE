---
title: setAsset
description: JavaScript-API-Referenz für den Videobild-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# setAsset{#setasset}

JavaScript-API-Referenz für den Videobild-Viewer.

` setAsset( *`asset`*)`

Legt das neue Asset fest. Sie können diesen Parameter jederzeit vor oder nach der `init()` aufrufen. Wenn es nach dem `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Assets</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} neue Asset-ID. </p> <p>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelbildreferenz:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
