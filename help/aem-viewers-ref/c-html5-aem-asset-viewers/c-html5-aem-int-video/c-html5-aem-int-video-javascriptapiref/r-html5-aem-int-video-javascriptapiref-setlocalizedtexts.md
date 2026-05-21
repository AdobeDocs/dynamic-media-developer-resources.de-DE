---
title: setLocalizedTexts
description: JavaScript-API-Referenz für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2fd557ad-088a-4ddc-8c00-b3cf3d2d9a2f
TQID: 'https://experienceleague.adobe.com/RQrzXGqP-pEfwAe5J7wnno7mK-R9NiSGTIlSlGiccQo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

JavaScript-API-Referenz für den interaktiven Video-Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

Legt die Werte der Lokalisierungssymbole für ein oder mehrere Gebietsschemata fest. Dieser Parameter muss vor dem `init()` aufgerufen werden.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> LocalizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSON-Objekt mit Lokalisierungsdaten. </p> <p>Weitere Informationen finden Sie unter Lokalisieren <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Elemente der Benutzeroberfläche </a>. </p> <p>Weitere Informationen zum <i> des -Objekts finden Sie </i> „Viewer-SDK-Benutzerhandbuch“ und im Beispiel . </p> </td> 
  </tr> 
 </tbody> 
</table>

Siehe auch [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
