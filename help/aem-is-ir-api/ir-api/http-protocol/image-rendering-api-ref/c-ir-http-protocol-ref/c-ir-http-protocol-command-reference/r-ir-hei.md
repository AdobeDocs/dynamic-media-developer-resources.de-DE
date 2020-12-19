---
description: Replizieren Sie die Bildhöhe. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbilds nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bilds beibehalten wird.
seo-description: Replizieren Sie die Bildhöhe. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbilds nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bilds beibehalten wird.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# hei{#hei}

Replizieren Sie die Bildhöhe. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbilds nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bilds beibehalten wird.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Replizieren Sie die Bildhöhe in Pixel (Ganzzahl größer als 0). </p></td> 
 </tr> 
</table>

Das Bild wird nicht eingefügt, wenn sowohl `wid=` als auch `hei=` angegeben sind und Breite/Höhe sich vom Seitenverhältnis des Bilds unterscheidet.

`wid=` und  `hei=` arbeiten Sie zusammen, um die Größe des Bildes zu definieren, das vom Server zurückgegeben wird. Wenn `scl=` nach `wid=` oder `hei=` in der URL kommt, werden diese Befehle abgebrochen und `scl=` definiert die Größe des vom Server zurückgegebenen Bildes.

Wenn `wid=` oder `hei=` nach `scl=` in der URL eingehen, brechen sie `scl=` ab und `wid=`/ `hei=` definieren die Größe des vom Server zurückgegebenen Bildes.

>[!NOTE]
>
>Wenn die berechnete oder standardmäßige Antwortbildgröße größer als `attribute::MaxPix` ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-6cbc6acd37c847beab84c896ac25280c}

Kann an einer beliebigen Stelle innerhalb der Anforderung auftreten. Wenn Sie die Bildgröße mit `wid=`, `hei=` oder `scl=` ändern, wird der Wert für die Druckauflösung, der im Antwortbild eingebettet ist, nicht geändert. Wird ignoriert, wenn `scl=` nach `wid=` und/oder `hei=` in der Befehlssequenz auftritt.

## Standard {#section-61043f6c1f5d450883ff9e5eafd95955}

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind, wird das Antwortbild so skaliert, dass es in die von `attribute::DefaultPix` definierte Größe passt. Wenn `attribute::DefaultPix` leer ist, hat das Antwortbild dieselbe Größe wie das Ansicht der Vignette.

## Verwandte Themen {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
