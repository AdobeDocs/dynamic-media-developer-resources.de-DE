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

---


# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Gibt den Palettentyp an. </p> <p>Auf <span class="codeph"> adaptiv einstellen, </span> um eine optimale Palette für das Bild zu berechnen. </p> <p>Auf <span class="codeph"> Web </span> oder <span class="codeph"> mac einstellen, </span> um eine vordefinierte Palette auszuwählen. </p> <p> <p>Hinweis:  Der <span class="codeph"> Mac- </span> Palettentyp wird nur für GIF- und PNG8-Formate unterstützt, nicht jedoch für GIF-Alpha- und PNG8-Alpha-Formate. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dither </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Gibt die Dithering-Optionen an. </p> <p>Auf <span class="codeph"> Diffusion </span> für Floyd-Steinberg-Fehlerdiffusion einstellen </p> <p>Auf <span class="codeph"> Aus einstellen, </span> um Dithering zu deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span></span> </p> </td> 
   <td colname="col2"> <p>Anzahl der Ausgangsfarben (2-256) </p> <p>Gibt an, wie viele Farben in der <span class="codeph"> Palette "adaptiv"enthalten </span> sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span></span> </p> </td> 
   <td colname="col2"> <p>Eine kommagetrennte Liste von erzwungenen RGB-Farben im Hex6-Format </p> <p>Hiermit können Sie Farben angeben, die in eine <span class="codeph"> adaptive </span> Palette eingeschlossen werden sollen. Wenn die Anzahl der angegebenen Farben kleiner als <span class="codeph"> numColors ist <span class="varname"></span> </span>, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8ab5035055b24b858270d260912a7f3d}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird nur verwendet, wenn `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`oder `fmt=png8-alpha`. Andernfalls ignoriert.

Die mit ` *`colorList`*` angegebenen Farben müssen aus RGB-Werten im hex6-Format bestehen (siehe ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) ohne Präfix &#39; `0x`&#39;. Andere Farbspezifikatoren sind nicht zulässig. *`numColors`* muss zwischen 2 und 256 liegen.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-e34aca7587d548a7ae9d4266b80c9451}

Erstellen Sie eine GIF-Miniaturansicht mit der `web` Palette und ohne Dithering:

` http:// *`Server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertieren Sie das Bild in ein bitonales GIF mit Key-Farbtransparenz und erzwingen Sie Farben in Schwarzweiß:

` http:// *`Server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Verwandte Themen {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
