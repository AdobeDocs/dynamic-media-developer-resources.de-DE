---
description: Hintergrundfarbe der Ansicht. Gibt die Hintergrundfarbe für das Composite-Bild (Ansicht) an.
seo-description: Hintergrundfarbe der Ansicht. Gibt die Hintergrundfarbe für das Composite-Bild (Ansicht) an.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

Hintergrundfarbe der Ansicht. Gibt die Hintergrundfarbe für das Composite-Bild (Ansicht) an.

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Farbe</span></span> </p> </td> 
  <td class="stentry"> <p>Farbwert Grau, RGB oder CMYK. </p></td> 
 </tr> 
</table>

Gibt eine undurchsichtige Füllfarbe für den Hintergrund der Ansicht an. Nur sichtbar, wenn das Composite-Bild transparente Bereiche hat oder wenn das Composite-Bild ein anderes Seitenverhältnis als das Rechteck Ansicht hat. Wird ignoriert, wenn `fmt=tif-alpha` oder `fmt=png-alpha`, oder `req=mask`.

>[!NOTE]
>
>Das Suffix &quot;s&quot;-Farbe wird ignoriert `bgc=`. Mit den angegebenen Farbwerten `bgc=` werden immer mit dem jeweiligen Ausgabefarbraum verknüpft.

## Eigenschaften {#section-b729b50b1ea7433b82ba34ecd61839cd}

Ansicht. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`oder `fmt=swf-alpha`.

Jeder mit Farbe angegebene Alpha-Wert wird ignoriert.

*`color`* wird angenommen, dass sie zum Ausgabefarbraum gehört (wie mit angegeben `icc=`) und denselben Pixeltyp wie das Ausgabebild haben sollte. Wenn die Pixeltypen nicht übereinstimmen, *`color`* wird mit naiver Konvertierung konvertiert.

## Standard {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Beispiel {#section-7bcdfbc0e1274e86a69d39186b090789}

Geben Sie eine explizite Hintergrundfarbe für eine Miniaturansichtsanforderung an:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Verwandte Themen {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Farbmanagement](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
