---
description: JavaScript-API-Referenz für den E-Katalog-Viewer.
solution: Experience Manager
title: eCatalogViewer
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 111699a3-8a70-4caf-b7da-7b594b785f7c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# eCatalogViewer{#ecatalogviewer}

JavaScript-API-Referenz für den E-Katalog-Viewer.

`eCatalogViewer([config])`

-Konstruktor erstellt eine neue eCatalog-Viewer-Instanz.

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> optionales JSON-Konfigurationsobjekt ermöglicht es allen Viewer-Einstellungen, an den Konstruktor zu übergeben, und verhindert, dass einzelne Setter-Methoden aufgerufen werden. Enthält die folgenden Eigenschaften: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span>  -  <span class="codeph"> {String}  </span> ID des DOM-Containers (normalerweise ein  <span class="codeph"> DIV  </span>), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn <span class="codeph"> init() </span> ausgeführt wird. Erforderlich. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON-Objekt mit Viewer-Konfigurationsparametern, bei denen der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder ein SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender settings-Wert ist. Erforderlich. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> Handler  </span> -  <span class="codeph"> {Object}  </span> JSON-Objekt mit Viewer-Ereignis-Rückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses ist und der Eigenschaftswert eine JavaScript-Funktionsreferenz zu einem entsprechenden Rückruf ist. Optional. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Ereignis-Rückrufe </a> . </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> lokalisierteTexte  </span> - {  <span class="codeph"> Object  </span>} JSON-Objekt mit Lokalisierungsdaten. Optional. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisierung von Benutzeroberflächenelementen </a> . </p> <p>Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer SDK-Benutzerhandbuch</i> und im Beispiel . </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
