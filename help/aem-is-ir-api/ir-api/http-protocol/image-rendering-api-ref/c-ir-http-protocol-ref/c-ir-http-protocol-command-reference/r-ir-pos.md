---
title: POS
description: Abziehposition. Definiert den Versatz in Zoll vom Ankerpunkt des Abziehbilds zum Abziehbildursprungspunkt, der durch das Vignettenzielobjekt definiert ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# POS{#pos}

Abziehposition. Definiert den Versatz in Zoll vom Ankerpunkt des Abziehbilds zum Abziehbildursprungspunkt, der durch das Vignettenzielobjekt definiert ist.

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Relative Positionsanpassung in Szenenkoordinateneinheiten (normalerweise Zoll) (real, real). </p></td> 
 </tr> 
</table>

## Eigenschaften {#section-50371cfa4e244bc49d2295a918749258}

Materialattribut. Ignoriert von anderen Materialien als Abziehbildern.

## Standard {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`. Richtet den Ankerpunkt des Abziehbilds am Abziehbild-Ursprung des Vignettenobjekts aus.

## Verwandte Themen {#section-7cd8139481334ed79704d628b5bbd236}

[Szenenkoordinaten](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [Anker=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
