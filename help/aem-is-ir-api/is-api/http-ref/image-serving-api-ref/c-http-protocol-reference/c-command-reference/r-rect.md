---
description: Rechteck der endgültigen Ansicht. Ermöglicht das Zerlegen der endgültigen Ansicht in mehrere Bänder oder Kacheln, die vom Kunden nahtlos und ohne Artefakte an den Rändern geliefert und wiederaufgebaut werden können.
seo-description: Rechteck der endgültigen Ansicht. Ermöglicht das Zerlegen der endgültigen Ansicht in mehrere Bänder oder Kacheln, die vom Kunden nahtlos und ohne Artefakte an den Rändern geliefert und wiederaufgebaut werden können.
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# rect{#rect}

Rechteck der endgültigen Ansicht. Ermöglicht das Zerlegen der endgültigen Ansicht in mehrere Bänder oder Kacheln, die vom Kunden nahtlos und ohne Artefakte an den Rändern geliefert und wiederaufgebaut werden können.

`rect= *``*, *``*[, *`coordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kohle</span> </p> </td> 
  <td class="stentry"> <p>Pixel-Versatz von der oberen linken Ecke des Ansicht-Bildes nach der Anwendung von <span class="varname"> "scale</span>"links oben im Rechteck "Ansicht"(int, int) in Pixel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Größe</span> </p></td> 
  <td class="stentry"> <p>Größe des ROI in Pixel (int, int). Gibt die Größe des Antwortbilds an. Das Bild wird mit <span class="codeph"> bgc=</span> in Bereichen gefüllt, die nicht vom Bild der Ansicht abgedeckt werden (oder transparent gelassen, wenn <span class="codeph"> fmt=*-alpha</span> in der Anforderung vorhanden ist). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Skalierungsfaktor (real). Werte, die kleiner als 1,0 sind, verringern die Auflösung und Werte größer als 1,0 erhöhen die Auflösung. </p></td> 
 </tr> 
</table>

Mit diesem Befehl kann Image Serving große Bilder über HTTP bereitstellen, die andernfalls die mit `attribute::MaxPix` konfigurierte Größenbeschränkung überschreiten würden.

>[!NOTE]
>
>Die besten Ergebnisse bei Verwendung der JPEG-Komprimierung erzielen Sie, wenn die Streifen- oder Kachelgröße ein Vielfaches der JPEG-Kodierungs-Kachelgröße (16 x 16 Pixel) ist.

## Beispiel {#section-932fcfcb41d74a29bc929e4430c49601}

Trennen Sie ein druckbares CMYK-Bild in mehrere Streifen mit voller Auflösung, um die Dateigröße zu reduzieren. Wenn wir ein zusammenhängendes Bild anfordern würden:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Zuerst werden relevante Informationen zum Bild abgerufen:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

Die Textantwort umfasst die folgenden Eigenschaften:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Anhand dieser Informationen entscheiden wir, dass wir vier Streifen im Format 600 x 2000 Pixel haben möchten. Der Befehl `rect=` wird zur Beschreibung der Bandgrößen und -positionen verwendet.

Da dieses Bild häufig geändert wird, werden wir den Befehl `id=` einschließen, um die Wahrscheinlichkeit zu minimieren, dass wir mit einem oder mehreren Streifen aus einer älteren Version des Bildes enden, die möglicherweise in einem CDN- oder Proxyserver zwischengespeichert wurden. Zu diesem Zweck wird der Wert der Eigenschaft `image.version` verwendet.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Eigenschaften {#section-aae223cee13e46d38b74680c048d945b}

Ansicht. Gilt unabhängig von der aktuellen Ebeneneinstellung.

Sämtliche Bereiche des ROI, die sich außerhalb des Bilds der Ansicht befinden, werden mit `bgc=` aufgefüllt.

Wichtig `rect=` wird *nach* der endgültigen Skalierung und Anpassung mit `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` und `align=` angewendet.

## Standard {#section-b296d3bbfb19441f87137a452b70f19a}

Gesamtes, unverändertes Ansicht-Image ( `rect=0,0,width,height,1.0`).

## Siehe auch {#section-74015202c0c545ec82aec614d74b4bbd}

[beschneiden=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [erweitern=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)  [align=, fit=,rgn=attribute::MaxPix,=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
