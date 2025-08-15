---
title: aufrecht
description: Rechteck in der endgültigen Ansicht. Damit kann das endgültige Ansichtsbild in mehrere Streifen oder Kacheln zerlegt werden, die separat geliefert und vom Kunden nahtlos und ohne Artefakte entlang der Ränder wieder zusammengesetzt werden können.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 1%

---

# aufrecht{#rect}

Rechteck in der endgültigen Ansicht. Damit kann das endgültige Ansichtsbild in mehrere Streifen oder Kacheln zerlegt werden, die separat geliefert und vom Kunden nahtlos und ohne Artefakte entlang der Ränder wieder zusammengesetzt werden können.

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Versatz von der linken oberen Ecke des Ansichtsbilds zur linken oberen Ecke des Ansichtsrechtecks (int, int), ausgedrückt in Pixeln, nach <span class="varname"> Skalierung </span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Größe</span> </p></td> 
  <td class="stentry"> <p>Größe des ROI in Pixeln (int, int). Gibt die Größe des Antwortbildes an. Das Bild wird mit <span class="codeph"> bgc=</span> in Bereichen gefüllt, die nicht vom Ansichtsbild abgedeckt werden (oder transparent gelassen, wenn <span class="codeph"> fmt=*-alpha</span> in der Anfrage vorhanden ist). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Skala</span> </p></td> 
  <td class="stentry"> <p>Skalierungsfaktor (real). Bei Werten kleiner als 1,0 wird die Auflösung reduziert, und bei Werten größer als 1,0 wird die Auflösung erhöht. </p></td> 
 </tr> 
</table>

Mit diesem Befehl kann Image Serving große Bilder über HTTP bereitstellen, die andernfalls die mit `attribute::MaxPix` konfigurierte Größenbeschränkung überschreiten würden.

>[!NOTE]
>
>Für optimale Ergebnisse sollte bei Verwendung der JPEG-Komprimierung die Streifen- oder Kachelgröße ein Vielfaches der JPEG-Kodierungs-Kachelgröße (16x16 Pixel) betragen.

## Beispiel {#section-932fcfcb41d74a29bc929e4430c49601}

Trennen Sie ein druckbares CMYK-Bild in mehrere Streifen mit voller Auflösung, um die Download-Dateigrößen zu reduzieren. Wenn Sie ein fortlaufendes Bild angefordert haben:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Zunächst werden relevante Informationen über das Bild abgerufen:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

Die Textantwort enthält die folgenden Eigenschaften:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Basierend auf diesen Informationen sind vier Bildstreifen mit 600x2000 Pixeln erwünscht. Der Befehl `rect=` wird verwendet, um die Streifengrößen und -positionen zu beschreiben.

Da dieses Bild häufig geändert wird, ist der `id=`-Befehl enthalten. Dadurch wird die Wahrscheinlichkeit minimiert, dass am Ende ein oder mehrere Streifen aus einer älteren Version des Bildes vorhanden sind, die möglicherweise in einem CDN oder Proxy-Server zwischengespeichert wurden. Der Wert der `image.version`-Eigenschaft wird für diesen Zweck verwendet.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Eigenschaften {#section-aae223cee13e46d38b74680c048d945b}

Attribut anzeigen. Sie gilt unabhängig von der aktuellen Ebeneneinstellung.

Alle Bereiche des ROI, die sich außerhalb des Ansichtsbilds erstrecken, werden mit `bgc=` aufgefüllt.

Wichtige `rect=` werden *nach* abschließender Skalierung und Anpassung mit `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` und `align=` angewendet.

## Standard {#section-b296d3bbfb19441f87137a452b70f19a}

Gesamtes, unverändertes Ansichtsbild ( `rect=0,0,width,height,1.0`).

## Siehe auch {#section-74015202c0c545ec82aec614d74b4bbd}

[Zuschneiden=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [Erweitern=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [WID=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [Align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
