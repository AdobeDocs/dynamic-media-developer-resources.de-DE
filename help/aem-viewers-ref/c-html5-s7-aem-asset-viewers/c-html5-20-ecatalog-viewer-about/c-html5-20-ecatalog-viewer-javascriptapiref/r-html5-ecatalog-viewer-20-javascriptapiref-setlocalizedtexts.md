---
description: JavaScript-API-Referenz für Video-Viewer.
seo-description: JavaScript-API-Referenz für Video-Viewer.
seo-title: setLocalizedTextes
solution: Experience Manager
title: setLocalizedTextes
topic: Dynamic media
uuid: c87e9f32-59f9-4f7a-a2cb-89813c00524b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# setLocalizedTexte{#setlocalizedtexts}

JavaScript-API-Referenz für Video-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-Objekt mit lokale Anpassungen-Daten. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokale Anpassung der Elemente der Benutzeroberfläche</a>. </p> <p>Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer-SDK-Benutzerhandbuch</i> und im Beispiel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt lokale Anpassung-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor `init()` aufgerufen werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

