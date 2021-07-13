---
description: Standardbild für Antworten. Gibt den Bild- oder Katalogeintrag an, der verwendet werden soll, falls eine Bilddatei nicht gefunden werden kann und defaultImage= in der Anfrage nicht angegeben ist.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# DefaultImage{#defaultimage}

Standardbild für Antworten. Gibt den Bild- oder Katalogeintrag an, der verwendet werden soll, falls eine Bilddatei nicht gefunden werden kann und defaultImage= in der Anfrage nicht angegeben ist.

Kann entweder ein Katalogeintrag (einschließlich einer Vorlage) oder ein relativer Pfad (zu `attribute::RootPath`) oder ein absoluter Bilddateipfad sein. Nützlich zum Ersetzen fehlender Bilder durch Standardbilder.

## Eigenschaften {#section-b6d8193827c34e5f948792aba8b8daaf}

Textzeichenfolge. Wenn angegeben, muss entweder ein gültiger `catalog::Id`-Wert in diesem Bildkatalog oder ein relativer Pfad (zu `attribute::RootPath`) oder ein absoluter Pfad zu einer Bilddatei sein, auf die der Image-Server zugreifen kann.

## Einschränkungen {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Ausländische Bildquellen werden vom standardmäßigen Bildmechanismus nicht abgedeckt. Wenn eine ausländische Bildquelle ungültig ist, wird ein Fehler zurückgegeben.

## Standard {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Vererbt von `default::DefaultImage` , falls nicht definiert. Wenn definiert, aber leer, wird das standardmäßige Bildverhalten deaktiviert, auch wenn `default::DefaultImage` definiert ist.

## Verwandte Themen {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
