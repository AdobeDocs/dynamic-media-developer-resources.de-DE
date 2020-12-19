---
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an.
seo-description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 7%

---


# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an.

` qlt= *``*[. *`qualitychroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Qualität </span> </p> </td> 
  <td class="stentry"> <p>Qualität der JPEG-Kodierung (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma  </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Farb-Downsampling (0 = normal, 1 = deaktiviert); optional ist, ist der Standardwert 0. </p> </td> 
 </tr> 
</table>

Gibt JPEG-Kodierungsattribute zur Steuerung der Komprimierungsstufe an. Dies wiederum ändert die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

Höhere *`quality`*-Werte erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigröße und verringern die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das *`chroma`*-Flag, um die für typische JPEG-Kodierer verwendete Farb-Downsampling zu deaktivieren. Dies kann die wahrgenommene Schärfe der Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons und nicht der Helligkeit definiert wird. Das Festlegen dieses Flag kann zu einer leichten Vergrößerung der Datei führen. Experimentieren Sie mit dieser Einstellung, wenn der Text etwas verschwommen aussieht.

## Eigenschaften {#section-897b61c786dd4230a2c5807f2f40e722}

Kann an beliebiger Stelle in der Anforderung auftreten.

Wird ignoriert, wenn das Ausgabebildformat keine JPEG-Komprimierung unterstützt. Eine Liste der Ausgabebildformate, die die JPEG-Komprimierung unterstützen, finden Sie in der Beschreibung von `fmt=`.

## Standard {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Verwandte Themen {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
