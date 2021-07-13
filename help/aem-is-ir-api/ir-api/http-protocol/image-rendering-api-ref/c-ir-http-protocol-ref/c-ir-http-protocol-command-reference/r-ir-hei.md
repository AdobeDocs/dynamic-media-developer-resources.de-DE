---
description: Antwortbildhöhe. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbilds nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bildes beibehalten wird.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---

# hei{#hei}

Antwortbildhöhe. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbilds nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bildes beibehalten wird.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Antwortbildhöhe in Pixel (Ganzzahl größer als 0). </p></td> 
 </tr> 
</table>

Das Bild wird nicht eingefügt, wenn sowohl `wid=` als auch `hei=` angegeben sind und Breite/Höhe sich vom Seitenverhältnis des Bildes unterscheiden.

`wid=` und  `hei=` arbeiten zusammen, um die Größe des vom Server zurückgegebenen Bildes zu definieren. Wenn `scl=` nach `wid=` oder `hei=` in der URL kommt, werden diese Befehle abgebrochen und `scl=` definiert die Größe des vom Server zurückgegebenen Bildes.

Wenn `wid=` oder `hei=` in der URL nach `scl=` kommt, brechen sie `scl=` ab und `wid=`/ `hei=` definieren die Größe des vom Server zurückgegebenen Bildes.

>[!NOTE]
>
>Wenn die berechnete oder standardmäßige Antwortbildgröße größer als `attribute::MaxPix` ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-6cbc6acd37c847beab84c896ac25280c}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Wenn Sie die Bildgröße mit `wid=`, `hei=` oder `scl=` ändern, wird der im Antwortbild eingebettete Wert für die Druckauflösung nicht geändert. Ignoriert, wenn `scl=` nach `wid=` und/oder `hei=` in der Befehlssequenz auftritt.

## Standard {#section-61043f6c1f5d450883ff9e5eafd95955}

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind, wird das Antwortbild so skaliert, dass es in die von `attribute::DefaultPix` definierte Größe passt. Wenn `attribute::DefaultPix` leer ist, hat das Antwortbild dieselbe Größe wie das Ansichtsbild der Vignette.

## Verwandte Themen {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
