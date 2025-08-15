---
title: quanteln
description: Farbquantisierung. Gibt Farbquantisierungsattribute für die Konvertierung der GIF-Ausgabe an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# quanteln{#quantize}

Farbquantisierung. Gibt Farbquantisierungsattribute für die Konvertierung der GIF-Ausgabe an.

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Typ </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Gibt den Palettentyp an. </p> <p>Legen Sie <span class="codeph"> adaptives </span> fest, um eine optimale Palette für das Bild zu berechnen. </p> <p>Auf <span class="codeph"> Web-</span> oder <span class="codeph"> Mac-</span> einstellen, um eine vordefinierte Palette auszuwählen. </p> <p> <p>Hinweis: Der <span class="codeph"> mac </span> Palettentyp wird nur für die Formate GIF und PNG8 unterstützt, jedoch nicht für die Formate GIF-Alpha und PNG8-Alpha.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Gibt die Dithering-Optionen an. </p> <p>Einstellung auf <span class="codeph"> diffuse </span> für Floyd-Steinberg-Fehlerdiffusion </p> <p>Legen Sie die Einstellung auf <span class="codeph"> aus </span> fest, um die Dithering-Funktion zu deaktivieren.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Anzahl Ausgabefarben (2-256) </p> <p>Gibt an, wie viele Farben in der <span class="codeph"> Palette für adaptive </span> enthalten sind.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>Eine kommagetrennte Liste erzwungener RGB-Farben im Hex6-Format </p> <p>Hier können Sie die Farben angeben, die in eine <span class="codeph"> Palette adaptiver </span> aufgenommen werden sollen. Wenn die Anzahl der angegebenen Farben kleiner als <span class="codeph"> <span class="varname"> numColors </span> </span> ist, werden zusätzliche Farben basierend auf dem Bildinhalt berechnet.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-8ab5035055b24b858270d260912a7f3d}

Anforderungsattribut. Sie gilt unabhängig von der aktuellen Ebeneneinstellung. Wird nur verwendet, wenn `fmt=gif`, `fmt=gif-alpha`, `fmt=png8` oder `fmt=png8-alpha`. Andernfalls ignoriert.

Die mit *`colorList`* angegebenen Farben müssen aus RGB-Werten im Hexadezimalformat 6 bestehen (siehe [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) ohne `0x`. Andere Farbspezifikatoren sind nicht zulässig. Der Modifikator *`numColors`* muss 2-256 sein.

## Standard {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Beispiel {#section-e34aca7587d548a7ae9d4266b80c9451}

Generieren Sie eine GIF-Miniaturansicht mithilfe der `web`-Palette ohne Dithering:

`http:// *`*Server*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Konvertieren Sie das Bild in eine zweifarbige GIF mit Schlüsselfarbtransparenz. Erzwingen Sie die Farben auf Schwarz und Weiß:

`http:// *`*Server*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## Verwandte Themen {#section-ea5e8de6084540cf86010370a4d0f01f}

[FMT=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
