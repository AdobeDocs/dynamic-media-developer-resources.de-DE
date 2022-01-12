---
title: setLocalizedTexte
description: JavaScript-API-Referenz für Flyout-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: abe33346-303a-4121-b41b-db89ae106e31
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 2%

---

# setLocalizedTexte{#setlocalizedtexts}

JavaScript-API-Referenz für Flyout-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objekt </span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Lokalisierung der Elemente der Benutzeroberfläche </a> für weitere Informationen. </p> <p>Siehe <i>Benutzerhandbuch zum Viewer-SDK</i> und das Beispiel für weitere Informationen zum Inhalt des Objekts. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt Lokalisierungs-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor aufgerufen werden `init()`.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```
