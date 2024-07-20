---
title: BasicZoomViewer
description: JavaScript-API-Referenz für einfachen Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 320f740e-c6b9-44d6-9369-9c2ec31189c5
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# BasicZoomViewer{#basiczoomviewer}

JavaScript-API-Referenz für einfachen Zoom-Viewer.

`BasicZoomViewer([config])`

Constructor erstellt eine einfache Zoom-Viewer-Instanz.

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> optionales JSON-Konfigurationsobjekt ermöglicht es allen Viewer-Einstellungen, an den Konstruktor zu übergeben, um zu verhindern, dass einzelne Setter-Methoden aufgerufen werden. Enthält die folgenden Eigenschaften: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> Kennung des DOM-Containers (normalerweise ein <span class="codeph"> DIV </span>), in den der Viewer eingefügt wird. Zum Zeitpunkt des Aufrufs dieser Methode ist es nicht erforderlich, dass das Containerelement erstellt wird. Der Container muss jedoch vorhanden sein, wenn <span class="codeph"> init() </span> ausgeführt wird. Erforderlich. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Konfigurationsparametern, bei denen der Eigenschaftsname entweder Viewer-spezifische Konfigurationsoption oder SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender settings-Wert ist. Erforderlich. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> Handler </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses und der Eigenschaftswert eine JavaScript-Funktionsreferenz zum entsprechenden Rückruf ist. Optional. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> Ereignisrückrufe </a> . </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexte </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Lokalisierungsdaten. Optional. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisierung der Elemente der Benutzeroberfläche </a> . </p> <p> Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer SDK-Benutzerhandbuch</i> und im Beispiel . Optional </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
