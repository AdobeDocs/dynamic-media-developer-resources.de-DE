---
description: Option zum Katalog-Abgleich.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# FullMatch{#fullmatch}

Option zum Katalog-Abgleich.

Ein Katalogeintrag wird in HTTP`*`Anfragen als `*/ *`rootId`*`imageId-Paar angegeben. Beim Analysieren wird ein Katalog ausgewählt, wenn `*`rootId`*` mit dem `attribute::RootId` des Katalogs übereinstimmt, und der Katalogdatensatz wird identifiziert, indem `*`imageId`*` mit einem `catalog::Id` Wert abgeglichen wird. Wenn ein Katalog gefunden wird, aber kein Katalogeintrag mit „imageId`*` übereinstimmt`*` kann der Server eine von zwei Aktionen ausführen:

Wenn `attribute::FullMatch` nicht festgelegt ist, verwendet der Server die Attribute des übereinstimmenden Katalogs. In diesem Fall wird `*`rootId`*` durch `attribute::RootPath` ersetzt (oder `default::RootPath`, falls nicht in diesem Katalog angegeben).

Wenn `attribute::FullMatch` festgelegt ist, ignoriert der Server den Katalog vollständig, als ob kein Katalog zugeordnet worden wäre, und fahren Sie mit den standardmäßigen Katalogattributen fort. In diesem Fall bleibt `*`rootId`*` Teil des Pfads (dem `default::RootPath` vorangestellt ist).

## Eigenschaften {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Markierung. Legen Sie hierfür 0 für das Standardverhalten oder 1 fest, um die vollständige Übereinstimmung zu ermöglichen.

## Standard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Von `default::FullMatch` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
