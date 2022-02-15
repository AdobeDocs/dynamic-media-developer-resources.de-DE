---
title: setLocalizedTexte
description: setLocalizedTexte
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 3bb1d277-e057-4a5d-9498-2adbca8f12b2
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# setLocalizedTexte{#setlocalizedtexts}

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objekt </span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Namespace des Viewer-SDK </a> für weitere Informationen. </p> <p>Siehe <i>Benutzerhandbuch zum Viewer-SDK</i> und das Beispiel für weitere Informationen zum Inhalt des Objekts. Optional. </p> </td> 
  </tr> 
 </tbody> 
</table>

Legt Lokalisierungs-SYMBOL-Werte für ein oder mehrere Gebietsschemas fest. Dieser Parameter muss vor aufgerufen werden `init()`.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
