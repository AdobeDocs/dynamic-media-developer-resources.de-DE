---
title: qlt
description: JPEG-Qualität. Gibt JPEG-Kodierungsattribute an, um die Komprimierungsstufe zu steuern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 7%

---

# qlt{#qlt}

JPEG-Qualität. Gibt JPEG-Kodierungsattribute an, um die Komprimierungsstufe zu steuern.

` qlt= *`Qualität`*[. *`Chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Qualität </span> </p> </td> 
  <td class="stentry"> <p>JPEG-Kodierungsqualität (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG Chromatizitäts-Downsampling (0=normal, 1=disable); optional ist, ist der Standardwert 0. </p> </td> 
 </tr> 
</table>

Gibt JPEG-Kodierungsattribute an, um die Komprimierungsstufe zu steuern. Dies ändert wiederum die Dateigröße (die Menge der Antwortdaten) und indirekt die visuelle Qualität des resultierenden Bildes.

Higher *`quality`* -Werte erhöhen die Dateigröße und -qualität, niedrigere Werte verringern die Dateigröße und die wahrgenommene Bildqualität. Bei Werten über 90 entstehen oft Bilder, die vom nicht komprimierten Bild kaum zu unterscheiden sind.

Legen Sie die *`chroma`* Markierung zum Deaktivieren des Chromatizitäts-Downsampling, das von typischen JPEG-Kodierern verwendet wird. Diese Einstellung kann die wahrgenommene Schärfe der Kanten in einem Bild erhöhen, wenn die Kante durch eine Änderung der Farbe und nicht durch die Helligkeit definiert wird. Das Festlegen dieses Flag kann zu einer leichten Vergrößerung der Datei führen. Experimentieren Sie mit dieser Einstellung, wenn Text etwas verschwommen scheint.

## Eigenschaften {#section-897b61c786dd4230a2c5807f2f40e722}

Kann an einer beliebigen Stelle in der Anfrage auftreten.

Wird ignoriert, wenn das Ausgabebildformat keine JPEG-Komprimierung unterstützt. Siehe Beschreibung von `fmt=` für eine Liste der Ausgabebildformate, die die JPEG-Komprimierung unterstützen.

## Standard {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Verwandte Themen {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
