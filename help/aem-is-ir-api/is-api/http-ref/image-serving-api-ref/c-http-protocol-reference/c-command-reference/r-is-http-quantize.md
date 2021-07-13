---
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
solution: Experience Manager
title: quantifizieren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>Gibt den Palettentyp an. </p> <p>Auf <span class="codeph"> adaptive </span> setzen, um eine optimale Palette für das Bild zu berechnen. </p> <p>Legen Sie <span class="codeph"> web </span> oder <span class="codeph"> mac </span> fest, um eine vordefinierte Palette auszuwählen. </p> <p> <p>Hinweis:  Der Palettentyp <span class="codeph"> mac </span> wird nur für GIF- und PNG8-Formate unterstützt, nicht aber für die Formate GIF-Alpha und PNG8-Alpha. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>Gibt die Dithering-Optionen an. </p> <p>Für Floyd-Steinberg-Fehlerdiffusion auf <span class="codeph"> diffuse </span> setzen </p> <p>Auf <span class="codeph"> von </span> setzen, um Dithering zu deaktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>Anzahl der Ausgabefarben (2-256) </p> <p>Gibt an, wie viele Farben in der Palette <span class="codeph"> adaptiv </span> enthalten sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>Eine kommagetrennte Liste mit erzwungenen RGB-Farben im Hexadezimalformat </p> <p>Ermöglicht die Angabe von Farben, die in eine Palette <span class="codeph"> adaptiver Elemente </span> aufgenommen werden sollen. Wenn die Anzahl der angegebenen Farben kleiner ist als <span class="codeph"> <span class="varname"> numColors </span> </span>, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8ab5035055b24b858270d260912a7f3d}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird nur verwendet, wenn `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` oder `fmt=png8-alpha`. Andernfalls ignoriert.

Die mit `*`colorList`*` angegebenen Farben müssen aus RGB-Werten im hexadezimalen Format (siehe ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`) ohne &quot;`0x`&quot;Präfix bestehen. Andere Farbspezifikatoren sind nicht zulässig. *`numColors`* muss zwischen 2 und 256 liegen.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-e34aca7587d548a7ae9d4266b80c9451}

Generieren Sie eine GIF-Miniaturansicht mithilfe der Palette `web` und ohne Dithering:

` http:// *`Server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertieren Sie das Bild in eine bitonale GIF-Datei mit Schlüsselfarbtransparenz und erzwingen Sie Farben in Schwarzweiß:

` http:// *`Server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Verwandte Themen {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
