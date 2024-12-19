---
title: setLocalizedTexts
description: JavaScript-API-Referenz für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8b471abe-df80-4601-bdcc-b7928418f351
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript-API-Referenz für Video Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> LocalizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Weitere Informationen finden Sie unter Lokalisieren <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Elemente </a> Benutzeroberfläche . </p> <p>Siehe auch <i>Viewer-SDK-</i>) und das Beispiel für weitere Informationen zum Inhalt des -Objekts. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt die Werte der Lokalisierungssymbole für ein oder mehrere Gebietsschemata fest. Dieser Parameter muss vor dem `init()` aufgerufen werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
