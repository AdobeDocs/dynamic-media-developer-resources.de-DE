---
title: hei
description: Höhe des Antwortbildes. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbildes nicht größer ist als der angegebene Wert, wobei das Seitenverhältnis des Bildes beibehalten wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
TQID: 'https://experienceleague.adobe.com/-sH3rlYycsZ36DheRgEpMUm6xSuUnY7s-3awUgdfloA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 1%

---

# hei{#hei}

Höhe des Antwortbildes. Gibt die Skalierung des gerenderten Bildes an, sodass die Höhe des Antwortbildes nicht größer ist als der angegebene Wert, wobei das Seitenverhältnis des Bildes beibehalten wird.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Val</span> </span> </p></td> 
  <td class="stentry"> <p>Höhe des Antwortbildes in Pixel (Ganzzahl größer als 0). </p></td> 
 </tr> 
</table>

Das Bild wird nicht aufgefüllt, wenn sowohl `wid=` als auch `hei=` angegeben sind und Breite/Höhe sich vom Seitenverhältnis des Bildes unterscheidet.

`wid=` und `hei=` definieren gemeinsam die Größe des vom Server zurückgegebenen Bildes. Wenn `scl=` nach `wid=` oder `hei=` in der URL erfolgt, werden diese Befehle abgebrochen und `scl=` die Größe des vom Server zurückgegebenen Bildes definiert.

Wenn `wid=` oder `hei=` jedoch nach dem `scl=` in der URL erfolgt, wird die `scl=` abgebrochen und `wid=`/`hei=` die Größe des vom Server zurückgegebenen Bildes definiert.

>[!NOTE]
>
>Ein Fehler wird zurückgegeben, wenn die berechnete oder standardmäßige Größe des Antwortbildes größer als `attribute::MaxPix` ist.

## Eigenschaften {#section-6cbc6acd37c847beab84c896ac25280c}

Kann überall in der Anfrage auftreten. Durch Ändern der Größe des Bildes mit `wid=`, `hei=` oder `scl=` wird der im Antwortbild eingebettete Wert für die Druckauflösung nicht geändert. Ignoriert, wenn `scl=` nach `wid=` und/oder `hei=` in der Befehlssequenz auftritt.

## Standard {#section-61043f6c1f5d450883ff9e5eafd95955}

Wenn `wid=`, `hei=` oder `scl=` nicht angegeben sind, wird das Antwortbild so skaliert, dass es in die von `attribute::DefaultPix` definierte Größe passt. Wenn `attribute::DefaultPix` leer ist, hat das Antwortbild dieselbe Größe wie das Ansichtsbild der Vignette.

## Verwandte Themen {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
