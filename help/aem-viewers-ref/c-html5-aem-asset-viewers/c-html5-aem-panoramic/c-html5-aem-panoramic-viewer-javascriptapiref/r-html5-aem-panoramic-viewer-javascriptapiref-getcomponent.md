---
title: getComponent
description: JavaScript-API-Referenz für Panorama-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# getComponent{#getcomponent}

JavaScript-API-Referenz für Panorama-Viewer

`getComponent(componentId)`


Gibt eine Referenz auf die Viewer-SDK-Komponente zurück, die vom Viewer verwendet wird. Die Webseite kann diese Methode verwenden, um das Verhalten des vordefinierten Viewers zu erweitern oder anzupassen. Rufen Sie diese Methode erst nach dem `initComplete` Viewer-Rückruf wurde ausgeführt, andernfalls kann die Komponente noch nicht von der Viewer-Logik erstellt werden.

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` eine ID der vom Viewer verwendeten Viewer-SDK-Komponente. Dieser Viewer unterstützt die folgenden Komponenten-IDs:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponenten-ID </p> </th> 
   <th colname="col2" class="entry"> <p>Name der Komponentenklasse des Viewer-SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Behälter </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> panoramicView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beim Arbeiten mit SDK-APIs ist es wichtig, den richtigen vollständig qualifizierten SDK-Namespace zu verwenden, wie hier beschrieben: [Namespace des Viewer-SDK](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zur Viewer-SDK-API .

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` einen Verweis auf die Viewer-SDK-Komponente. Die Methode gibt `null` wenn die `componentId` ist keine unterstützte Viewer-Komponente oder wenn die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
