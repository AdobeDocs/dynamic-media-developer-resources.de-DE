---
description: JPEG-Größe in KiloBytes. Gibt die maximale Größe der JPEG-Antwort in Kilobyte an.
seo-description: JPEG-Größe in KiloBytes. Gibt die maximale Größe der JPEG-Antwort in Kilobyte an.
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
topic: Scene7 Image Serving - Image Rendering API
uuid: 832163ca-0554-481d-b87f-bf322f415274
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# jpegSize{#jpegsize}

JPEG-Größe in KiloBytes. Gibt die maximale Größe der JPEG-Antwort in Kilobyte an.

`jpegSize= *`Größe`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Größe</span></span> </p> </td> 
  <td class="stentry"> <p>Größe in Kilobyte. </p></td> 
 </tr> 
</table>

Wenn dies auf einen positiven Wert festgelegt ist und die JPEG-Antwort mit der angegebenen JPEG-Qualität diesen Wert nicht überschreitet, wird dieses Bild als Antwort zurückgegeben. Andernfalls verringert sich die JPEG-Qualität, bis entweder ein Bild erzeugt wird, das in die angegebene Größe passt, oder bis festgestellt wird, dass es nicht passen kann. Im letzteren Fall schlägt die Anforderung mit einem Fehler fehl.

Der Wert 0 bedeutet, dass die Antwort nicht durch die Größe eingeschränkt wird.

Negative Werte sind nicht zulässig.

## Eigenschaften {#section-19e544e77d35478b98fe8666f27d6968}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn das Ausgabebildformat nicht JPEG ist.

## Standard {#section-198b798ed187453197e0969c641d6fb5}

0

## Beispiel {#section-46bf806fd3ef4875b7726df32b6f834d}

Die Garantiegröße ist nicht zu groß für die Bereitstellung auf einem Gerät mit begrenztem Speicher:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Verwandte Themen {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
