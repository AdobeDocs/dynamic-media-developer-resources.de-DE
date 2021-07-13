---
description: Skalierungsansicht. Skaliert das zusammengesetzte Bild um das Gegenteil von invFactor.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# scl{#scl}

Skalierungsansicht. Skaliert das zusammengesetzte Bild um das Gegenteil von invFactor.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>Umgekehrter Skalierungsfaktor (real größer als 0,0). </p></td> 
 </tr> 
</table>

Bei `scl=1` wird keine Skalierung angewendet. *`invFactor`* größer als 1,0 Downskala und kleiner als 1,0 vergrößert das Composite-Bild.

Wenn `scl=` angegeben ist und `wid=` und/oder `hei=` ebenfalls vorhanden sind, wird das Bild nach der Skalierung auf `wid=` und/oder `hei=` zugeschnitten.

>[!NOTE]
>
>Wenn die berechnete oder standardmäßige Antwortbildgröße größer als `attribute::MaxPix` ist, wird ein Fehler zurückgegeben.

## Eigenschaften {#section-60af012719db477db4a4703e9a6da5f5}

Attribut anzeigen. Gilt unabhängig von der aktuellen Ebeneneinstellung.

## Standard {#section-32502fa218a24e1f9c65f41c0260b56a}

Wenn weder `wid=`, `hei=` noch `scl=` angegeben sind, hat das Antwortbild entweder die Größe des zusammengesetzten Bildes oder `attribute::DefaultPix`, je nachdem, welcher Wert kleiner ist.

## Beispiel {#section-a33f6239476a4b438d939656ad99aa76}

Eine gängige Anwendung von `scl=` finden Sie im Beispiel unter [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) .

## Verwandte Themen {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
