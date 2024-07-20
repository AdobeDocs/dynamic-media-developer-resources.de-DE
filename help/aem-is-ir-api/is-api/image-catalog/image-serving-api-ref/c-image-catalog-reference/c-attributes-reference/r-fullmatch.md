---
description: Option für die Katalogzuordnung.
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

Option für die Katalogzuordnung.

Ein Katalogeintrag wird in HTTP-Anfragen als `*`rootId`*/ *`imageId`*` -Paar angegeben. Beim Analysieren wird ein Katalog ausgewählt, wenn `*`rootId`*` mit dem `attribute::RootId` -Wert des Katalogs übereinstimmt und der Katalogdatensatz durch Abgleich von `*`imageId`*` mit einem `catalog::Id` -Wert identifiziert wird. Wenn ein Katalog gefunden wird, aber kein Katalogeintrag mit `*`imageId`*` übereinstimmt, kann der Server eine der beiden folgenden Aktionen durchführen:

Wenn `attribute::FullMatch` nicht festgelegt ist, verwendet der Server die Attribute des übereinstimmenden Katalogs. In diesem Fall wird `*`rootId`*` durch `attribute::RootPath` (oder `default::RootPath` ersetzt, falls in diesem Katalog nicht angegeben).

Wenn `attribute::FullMatch` festgelegt ist, ignoriert der Server den Katalog vollständig, als wäre kein Katalog zugeordnet worden, und verwendet stattdessen die standardmäßigen Katalogattribute. In diesem Fall bleibt `*`rootId`*` Teil des Pfads (der durch `default::RootPath` vorangestellt wird).

## Eigenschaften {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Flag. Legen Sie für das Standardverhalten auf 0 oder auf 1 fest, um das vollständige Übereinstimmungsverhalten zu aktivieren.

## Standard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Wird von `default::FullMatch` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
