---
title: rect
description: Rechteck der endgültigen Ansicht. Dadurch kann das endgültige Ansichtsbild in mehrere Streifen oder Kacheln zerlegt werden, die vom Kunden getrennt und nahtlos neu zusammengestellt werden können, ohne dass Artefakte an den Kanten vorhanden sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---

# rect{#rect}

Rechteck der endgültigen Ansicht. Dadurch kann das endgültige Ansichtsbild in mehrere Streifen oder Kacheln zerlegt werden, die vom Kunden getrennt und nahtlos neu zusammengestellt werden können, ohne dass Artefakte an den Kanten vorhanden sind.

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixelversatz von der oberen linken Ecke des Ansichtsbilds oben links im Ansichtsrechteck (int, int), in Pixel angegeben, nach <span class="varname"> scale</span> angewendet wird. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Größe</span> </p></td> 
  <td class="stentry"> <p>Größe des ROI in Pixel (int, int). Gibt die Größe des Antwortbilds an. Das Bild wird mit <span class="codeph"> bgc=</span> in Bereichen, die nicht vom Ansichtsbild abgedeckt werden (oder transparent gelassen werden, wenn <span class="codeph"> fmt=*-alpha</span> in der Anfrage vorhanden ist). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Skalierungsfaktor (real). Werte, die kleiner als 1,0 sind, reduzieren die Auflösung, Werte größer als 1,0 erhöhen die Auflösung. </p></td> 
 </tr> 
</table>

Mit diesem Befehl kann Image Serving große Bilder über HTTP bereitstellen, die ansonsten die mit konfigurierte Größenbeschränkung überschreiten würden `attribute::MaxPix`.

>[!NOTE]
>
>Wenn die JPEG-Komprimierung verwendet wird, sollte die Streifen- oder Kachelgröße ein Vielfaches der JPEG-Kodierungs-Kachelgröße sein (16 x 16 Pixel).

## Beispiel {#section-932fcfcb41d74a29bc929e4430c49601}

Trennen Sie ein druckbares CMYK-Bild in mehrere Streifen mit voller Auflösung, um die Download-Dateigröße zu reduzieren. Wenn Sie ein zusammenhängendes Bild angefordert haben:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Zunächst werden relevante Informationen zum Bild abgerufen:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

Die Textantwort enthält folgende Eigenschaften:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Anhand dieser Informationen sind vier 600x2000 Pixelstreifen gewünscht. Die `rect=` -Befehl wird verwendet, um die Bandgrößen und -positionen zu beschreiben.

Da dieses Bild häufig geändert wird, wird die `id=` enthalten ist. Dadurch wird die Wahrscheinlichkeit minimiert, mit einem oder mehreren Streifen aus einer älteren Version des Bildes zu enden, die möglicherweise in einem CDN- oder Proxy-Server zwischengespeichert wurden. Der Wert der `image.version` -Eigenschaft zu diesem Zweck verwendet.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Eigenschaften {#section-aae223cee13e46d38b74680c048d945b}

Attribut anzeigen. Sie gilt unabhängig von der aktuellen Ebeneneinstellung.

Alle Bereiche des ROI, die sich außerhalb des Ansichtsbilds befinden, werden mit `bgc=`.

Wichtig `rect=` angewendet wird *after* endgültige Skalierung und Anpassung mit `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, und `align=`.

## Standard {#section-b296d3bbfb19441f87137a452b70f19a}

Gesamtes, unverändertes Ansichtsbild ( `rect=0,0,width,height,1.0`).

## Siehe auch {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [expand=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
