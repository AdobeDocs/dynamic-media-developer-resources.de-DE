---
description: JavaScript-API-Referenz für Video-Viewer.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic, Viewer, SDK/API, Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# setParams{#setparams}

JavaScript-API-Referenz für Video-Viewer.

` setParams( *`params`*)`

Legt einen oder mehrere Parameter auf einen bestimmten Wert fest. Die Methodenargument-Syntax ist mit einer URL-Abfrage identisch. Das heißt, sie repräsentiert Paare des Typs &quot;name=Wert&quot;, die durch `&` getrennt sind. Dasselbe wie in einer Abfrage-Zeichenfolge sind Namen und Werte in Prozent mit UTF8 kodiert. Bevor Sie `init()` aufrufen, muss dieser Parameter aufgerufen werden.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben werden.

Siehe auch [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value Parameterpaare, durch  <span class="codeph"> &amp;</span> getrennt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```

