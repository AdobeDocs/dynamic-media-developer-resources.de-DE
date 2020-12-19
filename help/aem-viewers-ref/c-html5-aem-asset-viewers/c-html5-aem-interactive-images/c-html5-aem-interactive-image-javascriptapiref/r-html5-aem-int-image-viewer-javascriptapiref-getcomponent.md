---
description: JavaScript-API-Referenz für Video-Bild-Viewer.
seo-description: JavaScript-API-Referenz für Video-Bild-Viewer.
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 6dd112f1-7b34-4d04-969e-b0cef46b4ad4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# getComponent{#getcomponent}

JavaScript-API-Referenz für Video-Bild-Viewer.

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
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beim Arbeiten mit SDK-APIs ist es wichtig, den richtigen voll qualifizierten SDK-Namensraum zu verwenden, wie unter [Viewer-SDK-Namensraum](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265) beschrieben.

Weitere Informationen zu einer bestimmten Komponente finden Sie in der Dokumentation zur Viewer SDK API.

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

`{Object}` eine Referenz zur Viewer-SDK-Komponente. Die Methode gibt `null` zurück, wenn `componentId` keine unterstützte Viewer-Komponente ist oder die Komponente noch nicht von der Viewer-Logik erstellt wurde.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

