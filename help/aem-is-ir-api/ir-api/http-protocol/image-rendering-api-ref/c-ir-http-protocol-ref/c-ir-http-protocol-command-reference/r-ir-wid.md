---
title: WID
description: Breite des Antwortbildes. Gibt die Skalierung des gerenderten Bildes an, sodass das Antwortbild nicht größer ist als der angegebene Wert, während das Seitenverhältnis des Bildes beibehalten wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# WID{#wid}

Breite des Antwortbildes. Gibt die Skalierung des gerenderten Bildes an, sodass das Antwortbild nicht größer ist als der angegebene Wert, während das Seitenverhältnis des Bildes beibehalten wird.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Val</span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0). </p></td> 
 </tr> 
</table>

Das Bild wird nicht aufgefüllt, wenn sowohl `wid=` als auch `hei=` angegeben sind und `wid`/`hei` sich vom Seitenverhältnis des Bildes unterscheidet.

`wid=` und `hei=` definieren gemeinsam die Größe des vom Server zurückgegebenen Bildes. Wenn `scl=` nach `wid=` oder `hei=` in der URL erfolgt, werden diese Befehle abgebrochen und `scl=` die Größe des vom Server zurückgegebenen Bildes definiert.

Wenn `wid=` oder `hei=` jedoch nach dem `scl=` in der URL erfolgt, wird die `scl=` abgebrochen und `wid=`/`hei=` die Größe des vom Server zurückgegebenen Bildes definiert.

>[!NOTE]
>
>Ein Fehler wird zurückgegeben, wenn die berechnete oder standardmäßige Größe des Antwortbildes größer als `attribute::MaxPix` ist.

## Eigenschaften {#section-2d067c6d371748e19cb157684700a49d}

Kann überall in der Anfrage auftreten. Durch Ändern der Größe des Bildes mit `wid=`, `hei=` oder `scl=` wird der im Antwortbild eingebettete Wert für die Druckauflösung nicht geändert. Ignoriert, wenn `scl=` nach `wid=` oder `hei=` in der Befehlssequenz auftritt.

## Standard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Wenn `wid=`, `hei=` oder `scl=` nicht angegeben sind, wird das Antwortbild so skaliert, dass es in die von `attribute::DefaultPix` definierte Größe passt. Wenn `attribute::DefaultPix` leer ist, hat das Antwortbild dieselbe Größe wie das Ansichtsbild der Vignette.

## Verwandte Themen {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
