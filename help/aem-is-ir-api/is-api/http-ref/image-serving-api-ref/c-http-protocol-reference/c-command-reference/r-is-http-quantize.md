---
title: quantifizieren
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# quantifizieren{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die GIF-Ausgabekonvertierung an.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Gibt den Palettentyp an. </p> <p>Auf <span class="codeph"> adaptive </span> setzen, um eine optimale Palette für das Bild zu berechnen. </p> <p>Setzen Sie dies auf <span class="codeph"> web </span> oder <span class="codeph"> mac </span> , um eine vordefinierte Palette auszuwählen. </p> <p> <p>Hinweis: Der Palettentyp <span class="codeph"> mac </span> wird nur für GIF- und PNG8-Formate unterstützt, nicht aber für GIF-Alpha- und PNG8-Alpha-Formate.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Gibt die Dithering-Optionen an. </p> <p>Für Floyd-Steinberg-Fehlerdiffusion auf <span class="codeph"> diffuse </span> setzen </p> <p>Setzen Sie dies auf <span class="codeph"> von </span> , um das Dithering zu deaktivieren.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Anzahl der Ausgabefarben (2-256) </p> <p>Gibt an, wie viele Farben in der Palette "<span class="codeph"> adaptiv </span>"enthalten sind.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Eine kommagetrennte Liste von erzwungenen RGB-Farben im Hexadezimalformat </p> <p>Ermöglicht die Angabe der Farben, die in die Palette <span class="codeph"> adaptiver Formulare </span> aufgenommen werden sollen. Wenn die angegebene Anzahl von Farben kleiner als <span class="codeph"> <span class="varname"> numColors </span> </span> ist, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8ab5035055b24b858270d260912a7f3d}

Anforderungsattribut. Sie gilt unabhängig von der aktuellen Ebeneneinstellung. Wird nur verwendet, wenn `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` oder `fmt=png8-alpha`. Andernfalls ignoriert.

Die mit *`colorList`* angegebenen Farben müssen aus RGB-Werten im Hexadezimalformat bestehen (siehe [Farbe](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) ohne das Präfix `0x`). Andere Farbspezifikatoren sind nicht zulässig. Der Modifikator *`numColors`* muss zwischen 2 und 256 liegen.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-e34aca7587d548a7ae9d4266b80c9451}

Generieren Sie eine GIF-Miniaturansicht mithilfe der Palette &quot;`web`&quot; und ohne Dithering:

`http:// *`*Server*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertieren Sie das Bild in eine bitonale GIF mit Schlüsselfarbtransparenz. Und Farben auf Schwarzweiß erzwingen:

`http:// *`*Server*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Verwandte Themen {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
