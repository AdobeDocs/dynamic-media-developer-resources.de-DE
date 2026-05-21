---
title: setLocalizedTexts
description: JavaScript-API-Referenz für Rotations-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 840c7e13-8998-4479-b0fc-f96a615a0a58
TQID: 'https://experienceleague.adobe.com/PX0DbOvWvloKR24x6FWI-4rEmRLoilbQ4oxRa7Qrzww'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript-API-Referenz für Rotations-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> LocalizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Weitere Informationen finden Sie unter Lokalisieren <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Elemente </a> Benutzeroberfläche . </p> <p>Weitere Informationen zum <i> des -Objekts finden Sie </i> „Viewer-SDK-Benutzerhandbuch“ und im Beispiel . </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt die Werte der Lokalisierungssymbole für ein oder mehrere Gebietsschemata fest. Dieser Parameter muss vor dem `init()` aufgerufen werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
