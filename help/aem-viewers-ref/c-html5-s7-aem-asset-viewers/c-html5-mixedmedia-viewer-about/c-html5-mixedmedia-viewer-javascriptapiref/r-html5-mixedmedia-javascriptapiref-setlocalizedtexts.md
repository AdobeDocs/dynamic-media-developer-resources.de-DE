---
description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-title: setLocalizedTextes
solution: Experience Manager
title: setLocalizedTextes
topic: Dynamic media
uuid: 86e2e70e-2147-4e63-9204-7a7a8566c3e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---


# setLocalizedTexte{#setlocalizedtexts}

JavaScript-API-Referenz für gemischte Medien-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-Objekt mit lokale Anpassungen-Daten. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Lokale Anpassung der Elemente der Benutzeroberfläche</a>. </p> <p>Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer-SDK-Benutzerhandbuch</i> und im Beispiel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt lokale Anpassung-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor `init()` aufgerufen werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

