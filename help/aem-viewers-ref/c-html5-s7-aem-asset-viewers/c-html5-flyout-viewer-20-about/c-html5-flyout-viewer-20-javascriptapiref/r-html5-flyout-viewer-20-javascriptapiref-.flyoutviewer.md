---
title: FlyoutViewer
description: JavaScript-API-Referenz für Flyout-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b64f16c8-03bf-4603-972f-845a4c1e2b02
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# FlyoutViewer{#flyoutviewer}

JavaScript-API-Referenz für Flyout-Viewer.

`FlyoutViewer([config])`

Konstruktor; erstellt eine Flyout-Viewer-Instanz.

## Parameter {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> optionales JSON-Konfigurationsobjekt ermöglicht es allen Viewer-Einstellungen, an den Konstruktor zu übergeben, und verhindert, dass einzelne Setter-Methoden aufgerufen werden. Enthält die folgenden Eigenschaften: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> Kennung des DOM-Containers (normalerweise eine <span class="codeph"> DIV </span>), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn <span class="codeph"> init() </span> ausgeführt wird. Erforderlich. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Konfigurationsparametern, bei denen der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder ein SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender settings-Wert ist. Erforderlich. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> Handler </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses ist und der Eigenschaftswert eine JavaScript-Funktionsreferenz zu einem entsprechenden Rückruf ist. Optional. <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Ereignisrückrufe </a> für weitere Informationen zu Viewer-Ereignissen. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexte </span> - { <span class="codeph"> Objekt </span>} JSON-Objekt mit Lokalisierungsdaten. Optional. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokalisierung der Elemente der Benutzeroberfläche </a> für weitere Informationen. </p> <p>Siehe <i>Benutzerhandbuch zum Viewer-SDK</i> und das Beispiel für weitere Informationen zum Inhalt des Objekts. Optional. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
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
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```
