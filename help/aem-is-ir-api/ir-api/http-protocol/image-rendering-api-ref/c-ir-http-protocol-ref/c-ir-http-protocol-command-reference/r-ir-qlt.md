---
title: qlt
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
TQID: 'https://experienceleague.adobe.com/T-e5oTA39GatOq7DkXIZPelLxnudZe3O1JYX0bOwlXk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 6%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an.

` qlt= *`quality`*[. *`chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Qualität der JPEG-Kodierung (1…100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Chromatizitäts-Downsampling (0=normal, 1=disable); optional, der Standardwert ist 0. </p> </td> 
 </tr> 
</table>

Gibt JPEG-Kodierungsattribute zur Steuerung des Komprimierungsgrads an. Dies wiederum variiert die Dateigröße (Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

Höhere *`quality`* erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigrößen und verringern die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Setzen Sie das Flag *`chroma`* , um die Chromatizitäts-Downsampling zu deaktivieren, die bei typischen JPEG-Encodern verwendet wird. Diese Einstellung kann die wahrgenommene Schärfe von Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung des Farbtons statt der Helligkeit definiert ist. Das Setzen dieses Flags kann zu einer leichten Erhöhung der Dateigröße führen. Experimentieren Sie mit dieser Einstellung, wenn der Text leicht unscharf erscheint.

## Eigenschaften {#section-897b61c786dd4230a2c5807f2f40e722}

Kann überall in der Anfrage auftreten.

Wird ignoriert, wenn das Bildformat der Ausgabe die JPEG-Komprimierung nicht unterstützt. Unter der Beschreibung von `fmt=` finden Sie eine Liste der Ausgabebildformate, die die JPEG-Komprimierung unterstützen.

## Standard {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Verwandte Themen {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)

