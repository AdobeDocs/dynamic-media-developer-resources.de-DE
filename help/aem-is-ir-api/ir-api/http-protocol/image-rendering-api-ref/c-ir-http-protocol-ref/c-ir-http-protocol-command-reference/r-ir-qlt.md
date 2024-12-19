---
title: qlt
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an.

` qlt= *`quality`*[. *`chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>JPEG-Kodierungsqualität (1…100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Chromatizitäts-Downsampling (0=normal, 1=disable); optional, Standard ist 0. </p> </td> 
 </tr> 
</table>

Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

Höhere *`quality`* erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigrößen und verringern die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das *`chroma`* Flag, um das Chromatizitäts-Downsampling zu deaktivieren, das bei herkömmlichen JPEG-Encodern verwendet wird. Diese Einstellung kann die wahrgenommene Schärfe von Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons statt der Helligkeit definiert ist. Das Setzen dieses Flags kann zu einer leichten Erhöhung der Dateigröße führen. Experimentieren Sie mit dieser Einstellung, wenn der Text leicht unscharf erscheint.

## Eigenschaften {#section-897b61c786dd4230a2c5807f2f40e722}

Kann überall in der Anfrage auftreten.

Wird ignoriert, wenn das Ausgabebildformat keine JPEG-Komprimierung unterstützt. Unter der Beschreibung von `fmt=` finden Sie eine Liste der Ausgabebildformate, die die JPEG-Komprimierung unterstützen.

## Standard {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Verwandte Themen {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
