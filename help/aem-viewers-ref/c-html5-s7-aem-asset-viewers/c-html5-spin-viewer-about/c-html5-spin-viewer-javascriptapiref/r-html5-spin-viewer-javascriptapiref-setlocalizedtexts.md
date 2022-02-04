---
title: setLocalizedTexte
description: JavaScript-API-Referenz für Rotationsset-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 840c7e13-8998-4479-b0fc-f96a615a0a58
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedTexte{#setlocalizedtexts}

JavaScript-API-Referenz für Rotationsset-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Objekt</span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Lokalisierung der Elemente der Benutzeroberfläche</a> für weitere Informationen. </p> <p>Siehe auch <i>Benutzerhandbuch zum Viewer-SDK</i> und das Beispiel für weitere Informationen zum Inhalt des Objekts. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt Lokalisierungs-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor aufgerufen werden `init()`.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
