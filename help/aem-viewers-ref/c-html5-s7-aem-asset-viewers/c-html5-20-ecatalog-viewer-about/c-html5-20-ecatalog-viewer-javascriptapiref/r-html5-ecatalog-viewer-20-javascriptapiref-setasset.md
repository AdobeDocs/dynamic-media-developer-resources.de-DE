---
title: setAsset
description: JavaScript-API-Referenz für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
TQID: 'https://experienceleague.adobe.com/vvkUPbunwRcV80Q7SNvUGaA-LAatPhxASa6y1wOz0eg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 1%

---

# setAsset{#setasset}

JavaScript-API-Referenz für Video Viewer.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} neue Asset-ID oder explizites Bildset mit optionalen Image-Serving-Modifikatoren, die nach dem <span class="codeph"> angehängt werden? </span>. </p> <p> Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt ein neues Asset fest. Sie können diesen Parameter jederzeit vor oder nach der `init()` aufrufen. Wenn es nach dem `init()` aufgerufen wird, tauscht der Viewer das Asset zur Laufzeit aus.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Einzelner Verweis auf ein Bildset, das in einem Katalog definiert ist:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Explizites Bildset mit vorkombinierten Seiten:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Explizites Bildset mit einzelnen Seitenbildern:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Scharfzeichnungsmodifikator wurde allen Bildern im Set hinzugefügt:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
