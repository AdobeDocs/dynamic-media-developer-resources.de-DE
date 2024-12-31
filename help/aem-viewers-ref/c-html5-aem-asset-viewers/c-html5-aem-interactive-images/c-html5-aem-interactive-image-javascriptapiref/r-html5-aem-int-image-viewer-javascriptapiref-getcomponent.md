---
title: getComponent
description: JavaScript-API-Referenz für den Videobild-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 5f2514a9-bbd0-436d-ad96-b89778604f8a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# getComponent{#getcomponent}

JavaScript-API-Referenz für den Videobild-Viewer.

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
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect-</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beim Arbeiten mit SDK-APIs ist es wichtig, den richtigen vollständig qualifizierten SDK-Namespace zu verwenden, wie unter [Viewer-SDK-Namespace](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265) beschrieben.

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zur Viewer-SDK-API .

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-SDK-Komponente. Die Methode gibt `null` zurück, wenn die `componentId` keine unterstützte Viewer-Komponente ist oder wenn die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```
