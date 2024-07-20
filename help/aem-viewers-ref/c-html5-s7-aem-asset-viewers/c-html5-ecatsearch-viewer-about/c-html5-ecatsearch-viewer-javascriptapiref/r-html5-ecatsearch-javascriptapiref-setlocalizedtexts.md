---
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
title: setLocalizedTexte
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: dfd57bde-70cd-483f-bcd4-680186e4a733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedTexte{#setlocalizedtexts}

JavaScript-API-Referenz für Video-Viewer.

[!DNL ` setLocalizedTexts( *`localizationInfo`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisierung der Elemente der Benutzeroberfläche</a> . </p> <p>Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer SDK-Benutzerhandbuch</i> und im Beispiel . </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt Lokalisierungs-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor [!DNL `init()`] aufgerufen werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
