---
title: qlt
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 6%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

` qlt= *`quality`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>JPEG-Kodierungsqualität (1…100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Chromatizitäts-Downsampling (0=normal, 1=disable); optional, Standard ist 0. </p> </td> 
 </tr> 
</table>

Höhere *`quality`* erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigrößen und verringern die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das *`chroma`* Flag, um das RGB-Chromatizitäts-Downsampling zu deaktivieren, das bei typischen JPEG-Encodern verwendet wird. Dies kann die wahrgenommene Schärfe von Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons anstatt der Helligkeit definiert ist. Das Setzen dieses Flags kann zu einer leichten Erhöhung der Dateigröße führen. Experimentieren Sie mit dieser Einstellung, wenn der Text leicht unscharf erscheint.

## Eigenschaften {#section-925a44cbdc9042db8d4eb149cd073d21}

Anforderungsattribut. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet. Wird ignoriert, wenn das Ausgabebilddateiformat keine JPEG-Kodierung unterstützt. Unter der Beschreibung von `fmt=` finden Sie Informationen darüber, welche Ausgabebildformate `qlt=` unterstützen.

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
