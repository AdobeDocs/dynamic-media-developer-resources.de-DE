---
title: WID
description: Breite des Antwortbildes. Gibt die Skalierung des gerenderten Bildes an, sodass das Antwortbild nicht größer ist als der angegebene Wert, während das Seitenverhältnis des Bildes beibehalten wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
TQID: 'https://experienceleague.adobe.com/9pR44QWe8G9qjTzNukUN0hEitEoGA47T3gbRUA6-Kpg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 235
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

