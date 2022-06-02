---
title: resMode
description: Resamplingmodus. Auswahl des Resampling- und/oder Interpolationsalgorithmus zur Skalierung von Bilddaten. Gilt auch für die Drehung von Textebenen und die Größenanpassung von zusammengesetzten Bildern während der Ansichtsumwandlung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# resMode{#resmode}

Resamplingmodus. Auswahl des Resampling- und/oder Interpolationsalgorithmus zur Skalierung von Bilddaten. Gilt auch für die Drehung von Textebenen und die Größenanpassung von zusammengesetzten Bildern während der Ansichtsumwandlung.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Wählt die standardmäßige bilineare Interpolation aus. schnellste Resamplingmethode; einige Aliasing-Artefakte sind sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation aus. CPU-intensiver als bi-lineare Interpolation, liefert jedoch schärfere Bilder mit weniger deutlichen Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos-Fensterfunktion als Interpolationsalgorithmus aus. Kann etwas schärfere Ergebnisse als bikubisch bei höheren CPU-Kosten erzielen. <span class="codeph"> scharf </span> ersetzt durch <span class="codeph"> sharp2 </span>, was eine geringere Wahrscheinlichkeit hat, Aliasing-Artefakte (Moiré) zu verursachen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bischarp </span> </p> </td> 
   <td colname="col2"> <p>Wählt Photoshop Standard-Resampler zum Reduzieren der Bildgröße aus, die in Adobe Photoshop als "bikubisch schärfer"bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>So halten Sie das Seitenverhältnis eines Bildes bei Verwendung von `resMode=bisharp` und `fit=stretch`, empfiehlt es sich, entweder den Breitenparameter oder den Höhenparameter zu verwenden. Wenn beide Parameter definiert werden müssen, können Sie sie wie im folgenden Beispiel in eine andere Ebene einschließen:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Eigenschaften {#section-a171bacf4ddf43c782e46b86a16d443e}

Anforderungsattribut. Gilt für alle Skalierungsvorgänge, die an der Erstellung des endgültigen Antwortbilds beteiligt sind, einschließlich aller Ebenen-Skalierung.

## Standard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Beispiel {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Rufen Sie eine hochwertige Ausgabe eines in einem Bildkatalog gespeicherten Bildes mit Ebenen ab. Das Bild kann Text enthalten. Das Bild wird in einer Bildbearbeitungsanwendung weiter verarbeitet und fordert daher einen Alphakanal mit dem Bild an.

` http:// *`Server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Verwandte Themen {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
