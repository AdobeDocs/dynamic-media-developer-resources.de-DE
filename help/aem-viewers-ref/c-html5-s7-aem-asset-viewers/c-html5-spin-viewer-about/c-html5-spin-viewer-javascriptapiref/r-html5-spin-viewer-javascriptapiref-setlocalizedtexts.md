---
description: JavaScript-API-Referenz für den Rotationsset-Viewer.
seo-description: JavaScript-API-Referenz für den Rotationsset-Viewer.
seo-title: setLocalizedTextes
solution: Experience Manager
title: setLocalizedTextes
topic: Dynamic media
uuid: bf136479-8ac8-4151-8911-377eed631aa2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedTextes{#setlocalizedtexts}

JavaScript-API-Referenz für den Rotationsset-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span></span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-Objekt mit Daten zur lokale Anpassung. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Lokale Anpassung der Elemente</a> der Benutzeroberfläche. </p> <p>Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer SDK-Benutzerhandbuch</i> und im Beispiel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt lokale Anpassung-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss zuvor aufgerufen werden `init()`.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

