---
description: Katalogzuordnungsoption.
seo-description: Katalogzuordnungsoption.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

Katalogzuordnungsoption.

Ein Katalogeintrag wird in HTTP-Anforderungen als ` *``*/ *`rootIdimageId`*` -Paar angegeben. Bei der Analyse wird ein Katalog ausgewählt, wenn ` *`rootId`*` mit dem `attribute::RootId` Wert des Katalogs übereinstimmt und der Katalogdatensatz durch Abgleich mit ` *`imageId`*` mit einem `catalog::Id` Wert identifiziert wird. Wenn ein Katalog gefunden wird, aber kein Katalogeintrag mit ` *`imageId`*`übereinstimmt, kann der Server eine der beiden folgenden Aufgaben ausführen:

Ist `attribute::FullMatch` dies nicht der Fall, verwendet der Server die Attribute des entsprechenden Katalogs. In diesem Fall wird die ` *`rootId`*` durch `attribute::RootPath` (oder `default::RootPath`, falls in diesem Katalog nicht angegeben) ersetzt.

Ist `attribute::FullMatch` dies der Fall, ignoriert der Server den Katalog vollständig, als wäre kein Katalog zugeordnet worden, und fährt mit den Standardkatalogattributen fort. In diesem Fall bleibt ` *`rootId`*` Teil des Pfads (der von vorangestellt wird `default::RootPath`).

## Eigenschaften {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Flag. Für das Standardverhalten auf 0 oder auf 1 setzen, um das vollständige Übereinstimmungsverhalten zu aktivieren.

## Standard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Vererbt von, `default::FullMatch` wenn nicht definiert oder leer.

## Verwandte Themen {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
