---
description: Breite des Antwortbilds. Gibt die Skalierung des gerenderten Bildes an, sodass das Antwortbild nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bilds beibehalten wird.
seo-description: Breite des Antwortbilds. Gibt die Skalierung des gerenderten Bildes an, sodass das Antwortbild nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bilds beibehalten wird.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

Breite des Antwortbilds. Gibt die Skalierung des gerenderten Bildes an, sodass das Antwortbild nicht größer als der angegebene Wert ist, wobei das Seitenverhältnis des Bilds beibehalten wird.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Bildbreite in Pixel (int größer als 0). </p></td> 
 </tr> 
</table>

Das Bild wird nicht eingefügt, wenn sowohl `wid=` als auch `hei=` angegeben ist und `wid`/ `hei` sich vom Seitenverhältnis des Bilds unterscheidet.

`wid=` und `hei=` arbeiten Sie zusammen, um die Größe des Bildes zu definieren, das vom Server zurückgegeben wird. Wenn die URL `scl=` hinter `wid=` oder `hei=` in der URL steht, werden diese Befehle abgebrochen und die Größe des vom Server zurückgegebenen Bildes `scl=` definiert.

Wenn die URL jedoch abbricht `wid=` oder `hei=` nach `scl=` ihr erscheint, wird die Größe des vom Server zurückgegebenen Bildes `scl=` / `wid=``hei=` definiert.

>[!NOTE]
>
>Wenn die berechnete oder standardmäßige Antwortbildgröße größer als `attribute::MaxPix`ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-2d067c6d371748e19cb157684700a49d}

Kann an einer beliebigen Stelle innerhalb der Anforderung auftreten. Wenn Sie die Größe des Bilds mit `wid=`, `hei=`oder `scl=` ohne Änderung des Wertes für die Druckauflösung ändern, der im Antwortbild eingebettet ist. Wird ignoriert, wenn `scl=` nach `wid=` oder `hei=` in der Befehlssequenz auftritt.

## Standard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Wenn weder `wid=`noch `hei=`oder `scl=` angegeben, wird das Antwortbild auf die durch `attribute::DefaultPix`diese Einstellung definierte Größe skaliert. Wenn `attribute::DefaultPix` das Antwortbild leer ist, hat es dieselbe Größe wie das Vignettenbild.

## Verwandte Themen {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
