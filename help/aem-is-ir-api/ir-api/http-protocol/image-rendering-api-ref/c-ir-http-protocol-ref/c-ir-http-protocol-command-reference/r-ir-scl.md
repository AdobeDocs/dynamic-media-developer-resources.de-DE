---
title: scl
description: Skalierungsansicht. Skaliert das gerenderte Bild um den angegebenen Skalierungsfaktor im Verhältnis zur Vignette mit voller Auflösung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# scl{#scl}

Skalierungsansicht. Skaliert das gerenderte Bild um den angegebenen Skalierungsfaktor im Verhältnis zur Vignette mit voller Auflösung.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Umgekehrter Skalierungsfaktor (real, 1,0 oder höher). </p></td> 
 </tr> 
</table>

Wenn `scl=` nach `wid=` oder `hei=` in der URL kommt, werden diese Befehle abgebrochen und `scl=` definiert die Größe des vom Server zurückgegebenen Bildes.

Wenn jedoch `wid=` oder `hei=` nach `scl=` in der URL kommt, brechen sie `scl=` ab und `wid=`/ `hei=` definieren die Größe des vom Server zurückgegebenen Bildes.

>[!NOTE]
>
>Wenn die berechnete oder standardmäßige Antwortbildgröße größer als `attribute::MaxPix` ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-170458cbd6984bd59a3434431258b20f}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Ignoriert, wenn `wid=` oder `hei=` in der Befehlssequenz nach `scl=` auftreten.

Wenn Sie die Bildgröße mit `scl=` ändern, wird der Wert für die Druckauflösung, der im Antwortbild eingebettet ist, nicht geändert.

## Standard {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Wenn `wid=`, `hei=` oder `scl=` nicht angegeben sind, wird das Antwortbild so skaliert, dass es in die durch `attribute::DefaultPix` definierte Größe passt. Wenn `attribute::DefaultPix` leer ist, hat das Antwortbild dieselbe Größe wie das Ansichtsbild der Vignette.

## Verwandte Themen {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
