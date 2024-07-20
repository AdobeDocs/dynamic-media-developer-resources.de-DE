---
title: getComponent
description: JavaScript API-Referenz für Inline-Zoom-Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 72ae83e4-b879-4b3b-a5d9-38ed0fc2969d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---

# getComponent{#getcomponent}

JavaScript API-Referenz für Inline-Zoom-Viewer

`getComponent(componentId)`

Gibt eine Referenz auf die Viewer-SDK-Komponente zurück, die vom Viewer verwendet wird. Die Webseite kann diese Methode verwenden, um das Verhalten des vordefinierten Viewers zu erweitern oder anzupassen. Rufen Sie diese Methode erst nach Ausführung des Viewer-Rückrufs `initComplete` auf. Andernfalls kann die Komponente noch nicht von der Viewer-Logik erstellt werden.

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
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> flyout </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Farbfelder </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beim Arbeiten mit SDK-APIs ist es wichtig, den vollständig qualifizierten SDK-Namespace ordnungsgemäß zu verwenden, wie in [Viewer-SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-namespace.md#concept-5af3b472b320496d87735ea612edda80) beschrieben.

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zum Viewer-SDK .

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Ein Verweis auf die Viewer-SDK-Komponente. Die Methode gibt `null` zurück, wenn die `componentId` keine unterstützte Viewer-Komponente ist oder wenn die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```
