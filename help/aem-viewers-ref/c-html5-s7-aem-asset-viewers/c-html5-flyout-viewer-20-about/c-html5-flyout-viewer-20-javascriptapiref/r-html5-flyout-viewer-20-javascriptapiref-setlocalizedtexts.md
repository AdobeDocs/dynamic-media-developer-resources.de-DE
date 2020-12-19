---
description: JavaScript-API-Referenz für Flyout-Viewer.
seo-description: JavaScript-API-Referenz für Flyout-Viewer.
seo-title: setLocalizedTextes
solution: Experience Manager
title: setLocalizedTextes
topic: Dynamic media
uuid: 69341735-5ebe-4e3b-acad-b6b916b11bb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---


# setLocalizedTexte{#setlocalizedtexts}

JavaScript-API-Referenz für Flyout-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSON-Objekt mit lokale Anpassungen-Daten. </p> <p>Weitere Informationen finden Sie unter <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokale Anpassung der Benutzeroberflächenelemente </a>. </p> <p>Weitere Informationen zum Inhalt des Objekts finden Sie im <i>Viewer-SDK-Benutzerhandbuch</i> und im Beispiel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt lokale Anpassung-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor `init()` aufgerufen werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

