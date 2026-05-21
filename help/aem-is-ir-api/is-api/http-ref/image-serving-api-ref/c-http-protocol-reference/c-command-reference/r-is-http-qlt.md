---
title: qlt
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
TQID: 'https://experienceleague.adobe.com/e7zzYHSi7X5tdPAy-0CWTK-Wqs5nfhEDLs2HYJ1D-f4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 6%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

` qlt= *`quality`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Qualität der JPEG-Kodierung (1…100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Chromatizitäts-Downsampling (0=normal, 1=disable); optional, der Standardwert ist 0. </p> </td> 
 </tr> 
</table>

Höhere *`quality`* erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigrößen und verringern die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das Flag *`chroma`* , um die RGB-Chromatizitäts-Downsampling zu deaktivieren, die bei typischen JPEG-Codierern verwendet wird. Dies kann die wahrgenommene Schärfe von Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons anstatt der Helligkeit definiert ist. Das Setzen dieses Flags kann zu einer leichten Erhöhung der Dateigröße führen. Experimentieren Sie mit dieser Einstellung, wenn der Text leicht unscharf erscheint.

## Eigenschaften {#section-925a44cbdc9042db8d4eb149cd073d21}

Anforderungsattribut. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet. Wird ignoriert, wenn das Ausgabebilddateiformat die JPEG-Kodierung nicht unterstützt. Unter der Beschreibung von `fmt=` finden Sie Informationen darüber, welche Ausgabebildformate `qlt=` unterstützen.

*`chroma`* wird ignoriert, wenn der Ausgabepixeltyp CMYK oder Grau ist.

## Standard {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Beispiel {#section-d7d33871d401433aa51d028823eae7a9}

Geringere Qualität für eine schnellere Übertragung über eine Verbindung mit geringer Bandbreite:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Höhere Qualität für Verbindungen mit hoher Bandbreite:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Verwandte Themen {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
