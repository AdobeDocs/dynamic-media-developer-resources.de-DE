---
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an. Dies wiederum ändert die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 6%

---


# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an. Dies wiederum ändert die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Qualität </span> </p> </td> 
  <td class="stentry"> <p>Qualität der JPEG-Kodierung (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma  </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Farb-Downsampling (0 = normal, 1 = deaktiviert); optional ist, ist der Standardwert 0. </p> </td> 
 </tr> 
</table>

Höhere *`quality`*-Werte erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigröße und verringern die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das *`chroma`*-Flag, um die RGB-Farbwertanpassung zu deaktivieren, die von typischen JPEG-Kodierern verwendet wird. Dies kann die wahrgenommene Schärfe der Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons und nicht der Helligkeit definiert wird. Das Festlegen dieses Flag kann zu einer leichten Vergrößerung der Datei führen. Experimentieren Sie mit dieser Einstellung, wenn der Text etwas verschwommen aussieht.

## Eigenschaften {#section-925a44cbdc9042db8d4eb149cd073d21}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn das Format der Ausgabebilddatei keine JPEG-Kodierung unterstützt. Informationen darüber, welche Ausgabebildformate &lt; a1/> unterstützen, finden Sie in der Beschreibung von `fmt=`.`qlt=`

*`chroma`* wird ignoriert, wenn der Ausgabepixeltyp CMYK oder Grau ist.

## Standard {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Beispiel {#section-d7d33871d401433aa51d028823eae7a9}

Geringere Qualität für schnellere Übertragung über eine Verbindung mit niedriger Bandbreite:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Verbessern Sie die Qualität von Verbindungen mit hoher Bandbreite:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Verwandte Themen {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
