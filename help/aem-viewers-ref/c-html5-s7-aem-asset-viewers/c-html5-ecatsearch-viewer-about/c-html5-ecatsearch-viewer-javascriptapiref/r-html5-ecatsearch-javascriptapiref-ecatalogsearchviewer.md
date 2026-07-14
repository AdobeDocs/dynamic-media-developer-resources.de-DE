---
description: JavaScript-API-Referenz für eCatalog SearchViewer.
solution: Experience Manager
title: eCatalogSearchViewer
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a7289d23-b2f6-4730-99fa-331174968e05
TQID: 'https://experienceleague.adobe.com/mpH1chEHyol7OHeHtR57-rCGYvEM43B2zz2t-ld11zA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 3%

---

# eCatalogSearchViewer{#ecatalogsearchviewer}

JavaScript-API-Referenz für eCatalog SearchViewer.

[!DNL `eCatalogSearchViewer([config])`]

Der -Konstruktor erstellt eine neue E-Katalog-Such-Viewer-Instanz.

## Parameter {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Konfiguration </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> optionales JSON-Konfigurationsobjekt ermöglicht es Ihnen, alle Viewer-Einstellungen an den Konstruktor zu übergeben und den Aufruf einzelner Setter-Methoden zu vermeiden. Enthält die folgenden Eigenschaften: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID des DOM-Containers (normalerweise ein <span class="codeph"> DIV-</span>), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Container-Element zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn <span class="codeph"> init()-</span> ausgeführt wird. Erforderlich. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Konfigurationsparametern, wobei der Eigenschaftsname entweder eine Viewer-spezifische Konfigurationsoption oder ein SDK-Modifikator ist und der Wert dieser Eigenschaft ein entsprechender Einstellungswert ist. Erforderlich. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph">-Handler </span> - <span class="codeph"> {Object} </span> JSON-Objekt mit Viewer-Ereignisrückrufen, wobei der Eigenschaftsname der Name des unterstützten Viewer-Ereignisses ist und der Eigenschaftswert ein JavaScript-Funktionsverweis auf einen entsprechenden Rückruf ist. Optional. </p> <p>Weitere Informationen zu Viewer-Ereignissen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> </a> zu Ereignis-Callbacks . </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedTexts-</span> - { <span class="codeph"> Object </span>} JSON-Objekt mit Lokalisierungsdaten. Optional. </p> <p>Weitere Informationen finden Sie unter Lokalisieren <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Elemente der Benutzeroberfläche </a>. </p> <p>Weitere Informationen zum <i> des -Objekts finden Sie </i> „Viewer-SDK-Benutzerhandbuch“ und im Beispiel . </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
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

