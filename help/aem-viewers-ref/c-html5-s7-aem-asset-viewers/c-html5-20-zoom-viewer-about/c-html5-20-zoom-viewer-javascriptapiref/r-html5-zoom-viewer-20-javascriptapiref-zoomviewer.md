---
title: ZoomViewer
description: JavaScript-API-Referenz für Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: fa52a017-0748-4e4f-8d91-ad1529fbfbdb
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---

# ZoomViewer{#zoomviewer}

JavaScript-API-Referenz für Zoom-Viewer.

`ZoomViewer([config])`

Der -Konstruktor erstellt eine Zoom-Viewer-Instanz.

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Konfiguration </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> optionalen JSON-Konfigurationsobjekt übergeben alle Viewer-Einstellungen an den Konstruktor, um den Aufruf einzelner Setter-Methoden zu vermeiden. Enthält die folgenden Eigenschaften: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID des DOM-Containers (normalerweise ein <span class="codeph"> DIV </span>), in den der Viewer eingefügt wird. Zum Zeitpunkt des Aufrufs dieser Methode ist es nicht erforderlich, dass das Container-Element erstellt wird. Der Container muss jedoch vorhanden sein, wenn <span class="codeph"> init()-</span> ausgeführt wird. Erforderlich. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Konfigurationsparametern, wobei der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder ein SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender Einstellungswert ist. Erforderlich. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph">-Handler </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Ereignisrückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert ein JavaScript-Funktionsverweis auf den entsprechenden Rückruf ist. Optional. <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> </a> zu Ereignis-Callbacks . </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> localizedTexts-</span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Lokalisierungsdaten. Optional. <p>Weitere Informationen finden Sie unter Lokalisieren <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Elemente der Benutzeroberfläche </a>. </p> <p>Siehe auch <i>Viewer-SDK-</i>) und das Beispiel für weitere Informationen zum Inhalt des -Objekts. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```
