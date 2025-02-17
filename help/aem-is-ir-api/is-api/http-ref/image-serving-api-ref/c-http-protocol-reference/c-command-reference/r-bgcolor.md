---
title: bgColor
description: Hintergrundfarbe der Ebene. Gibt die Hintergrundfarbe und Deckkraft der aktuellen Ebene an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 22c957e6-1a82-43a7-8467-871a150e7453
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# bgColor{#bgcolor}

Hintergrundfarbe der Ebene. Gibt die Hintergrundfarbe und Deckkraft der aktuellen Ebene an.

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Farbe</span></span> </p> </td> 
  <td class="stentry"> <p>Grau-, RGB- oder CMYK-Farbwert, mit oder ohne Alpha. </p></td> 
 </tr> 
</table>

Transparente und halb-opake Bereiche innerhalb des Begrenzungsrechtecks der Ebene werden mit der angegebenen Farbe* gefüllt, nachdem `opac=`, `rotate=` und `extend=` angewendet wurden.

## Eigenschaften {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Ebenenattribut. Gilt für die aktuelle Ebene oder für Ebene 0, falls `layer=comp`. Von Effektebenen ignoriert.

Es wird davon ausgegangen, dass *`color`* im Arbeitsfarbraum vorhanden ist, der dem Pixeltyp des *`color`* entspricht. *`color`* wird genau konvertiert, wenn das endgültige Ebenenbild einen anderen Pixeltyp aufweist.

## Standard {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (vollständig transparent).

## Beispiel {#section-6e14fcf1d31e432dbdb56b9320904453}

Siehe [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Verwandte Themen {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423), [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [color management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
