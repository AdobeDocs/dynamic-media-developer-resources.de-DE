---
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
seo-description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
seo-title: quantifizieren
solution: Experience Manager
title: quantifizieren
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---


# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>Gibt den Palettentyp an. </p> <p>Auf <span class="codeph"> adaptive </span> setzen, um eine optimale Palette für das Bild zu berechnen. </p> <p>Auf <span class="codeph"> web </span> oder <span class="codeph"> mac </span> setzen, um eine vordefinierte Palette auszuwählen. </p> <p> <p>Hinweis:  Der Palettentyp <span class="codeph"> mac </span> wird nur für die Formate GIF und PNG8 unterstützt, nicht jedoch für die Formate GIF-Alpha und PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>Gibt die Dithering-Optionen an. </p> <p>Für Floyd-Steinberg-Fehlerdiffusion auf <span class="codeph"> diffuse </span> setzen </p> <p>Auf <span class="codeph"> von </span> setzen, um das Dithering zu deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Anzahl der Ausgangsfarben (2-256) </p> <p>Gibt an, wie viele Farben in der Palette <span class="codeph"> für adaptive </span> enthalten sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>Eine kommagetrennte Liste von erzwungenen RGB-Farben im Hex6-Format </p> <p>Ermöglicht die Angabe von Farben, die in eine adaptive Palette <span class="codeph"> eingeschlossen werden sollen. </span> Wenn die angegebene Anzahl von Farben kleiner als <span class="codeph"> <span class="varname"> numColors </span> </span> ist, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8ab5035055b24b858270d260912a7f3d}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird nur verwendet, wenn `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` oder `fmt=png8-alpha`. Andernfalls ignoriert.

Die mit ` *`colorList`*` angegebenen Farben müssen aus RGB-Werten im hex6-Format (siehe ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) ohne Präfix &#39; `0x`&#39; bestehen. Andere Farbspezifikatoren sind nicht zulässig. *`numColors`* muss zwischen 2 und 256 liegen.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-e34aca7587d548a7ae9d4266b80c9451}

Generieren Sie eine GIF-Miniaturansicht mit der Palette `web` und ohne Dithering:

` http:// *`Server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertieren Sie das Bild in eine bitonale GIF-Datei mit Key-Farbtransparenz und erzwingen Sie Farben in Schwarzweiß:

` http:// *`Server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Verwandte Themen {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
