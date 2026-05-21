---
title: resMode
description: Resampling-Modus. Wählt den Resampling- und/oder Interpolationsalgorithmus für die Skalierung von Bilddaten. Gilt auch für die Drehung von Textebenen und die Größenanpassung von zusammengesetzten Bildern während der Ansichtstransformation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
TQID: 'https://experienceleague.adobe.com/uT9SBMqQ0JvU-S8BF2y0kY6C--jNhvggbRwhTpTJOGg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 1%

---

# resMode{#resmode}

Resampling-Modus. Wählt den Resampling- und/oder Interpolationsalgorithmus für die Skalierung von Bilddaten. Gilt auch für die Drehung von Textebenen und die Größenanpassung von zusammengesetzten Bildern während der Ansichtstransformation.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bilin </span> </p> </td> 
   <td colname="col2"> <p>Wahl der standardmäßigen bilinearen Interpolation Schnellste Resampling-Methode; einige Aliasing-Artefakte sind auffällig. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bicub-</span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation. CPU-intensiver als bilineare Interpolation, liefert jedoch schärfere Bilder mit weniger bemerkbaren Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Sharp2-</span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos-Fensterfunktion als Interpolationsalgorithmus. Kann zu einem höheren CPU-Preis etwas schärfere Ergebnisse als bikubische liefern. <span class="codeph"> scharfe </span> wurde durch <span class="codeph"> scharfe2-</span> ersetzt, wodurch die Wahrscheinlichkeit, Alias-Artefakte zu verursachen, geringer ist (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bisharp </span> </p> </td> 
   <td colname="col2"> <p>Wählt den standardmäßigen Photoshop-Resampler zur Reduzierung der Bildgröße, der in Adobe Photoshop als „bikubisch schärfer“ bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Um das Seitenverhältnis eines Bildes beizubehalten, wenn Sie sowohl `resMode=bisharp` als auch `fit=stretch` verwenden, empfiehlt es sich, entweder den Parameter „width“ oder den Parameter „height“ zu verwenden. Wenn beide Parameter definiert werden müssen, können Sie sie in eine andere Ebene einschließen, wie im folgenden Beispiel gezeigt:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Eigenschaften {#section-a171bacf4ddf43c782e46b86a16d443e}

Anforderungsattribut. Gilt für alle Skalierungsvorgänge, die an der Erstellung des endgültigen Antwortbildes beteiligt sind, einschließlich der gesamten Ebenenskalierung.

## Standard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Beispiel {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Rufen Sie eine hochwertige Ausgabedarstellung eines mehrschichtigen Bildes ab, das in einem Bildkatalog gespeichert ist. Das Bild kann Text enthalten. Das Bild wird in einer Bildbearbeitungsanwendung weiterverarbeitet und somit mit dem Bild einen Alphakanal angefordert.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Verwandte Themen {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
