---
description: Resamplingmodus. Wählen Sie den Resampling- und/oder Interpolationsalgorithmus, der zum Skalieren von Bilddaten verwendet werden soll. Gilt auch für die Drehung von Textebenen und die Größenanpassung von Composite-Bildern während der Transformation der Ansicht.
seo-description: Resamplingmodus. Wählen Sie den Resampling- und/oder Interpolationsalgorithmus, der zum Skalieren von Bilddaten verwendet werden soll. Gilt auch für die Drehung von Textebenen und die Größenanpassung von Composite-Bildern während der Transformation der Ansicht.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 16%

---


# resMode{#resmode}

Resamplingmodus. Wählen Sie den Resampling- und/oder Interpolationsalgorithmus, der zum Skalieren von Bilddaten verwendet werden soll. Gilt auch für die Drehung von Textebenen und die Größenanpassung von Composite-Bildern während der Transformation der Ansicht.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Wählt die standardmäßige bi-lineare Interpolation aus. Schnellste Neuberechnungsmethode; einige Aliasing-Artefakte sind möglicherweise bemerkbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation aus. CPU-intensiver als bilineare Interpolation, liefert aber schärfere Bilder mit weniger bemerkbaren Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos-Fensterfunktion als Interpolationsalgorithmus aus. Kann etwas schärfere Ergebnisse als „bikubisch“ erzeugen, lastet aber die CPU stärker aus. <span class="codeph"> spitze  </span> wurde durch  <span class="codeph"> sharp2 ersetzt  </span>, was eine geringere Wahrscheinlichkeit hat, Aliasartefakte zu verursachen (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Wählt Photoshop Standard-Resampler zum Reduzieren der Bildgröße aus, der in Adobe Photoshop als "bikubischer Scharfzeichner"bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-a171bacf4ddf43c782e46b86a16d443e}

Anforderungsattribut. Gilt für alle Skalierungsvorgänge, die mit der Erstellung des endgültigen Antwortbilds verbunden sind, einschließlich der Skalierung aller Ebenen.

## Standard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Beispiel {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Rufen Sie eine qualitativ hochwertige Darstellung eines in einem Bildkatalog gespeicherten Bildes mit Ebenen ab. Das Bild kann Text enthalten. Wir rechnen damit, dass die Bearbeitung in einer Bildbearbeitungsanwendung fortgesetzt wird, und fordern daher einen Alpha-Kanal mit dem Bild an.

` http:// *`Server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Verwandte Themen {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
