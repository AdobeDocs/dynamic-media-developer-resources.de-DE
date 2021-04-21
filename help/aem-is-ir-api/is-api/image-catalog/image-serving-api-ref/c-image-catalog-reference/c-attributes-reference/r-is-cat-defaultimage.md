---
description: Standardbild für Antwort. Gibt das Bild oder den Katalogeintrag an, der verwendet werden soll, wenn eine Bilddatei nicht gefunden werden kann und defaultImage= in der Anforderung nicht angegeben ist.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# DefaultImage{#defaultimage}

Standardbild für Antwort. Gibt das Bild oder den Katalogeintrag an, der verwendet werden soll, wenn eine Bilddatei nicht gefunden werden kann und defaultImage= in der Anforderung nicht angegeben ist.

Kann entweder ein Katalogeintrag (einschließlich einer Vorlage) oder ein relativer Pfad (zu `attribute::RootPath`) oder ein absoluter Bilddateipfad sein. Nützlich zum Ersetzen fehlender Bilder durch Standardbilder.

## Eigenschaften {#section-b6d8193827c34e5f948792aba8b8daaf}

Textzeichenfolge. Wenn angegeben, muss entweder ein gültiger `catalog::Id`-Wert in diesem Bildkatalog oder ein relativer (zu `attribute::RootPath`) oder ein absoluter Pfad zu einer Bilddatei sein, auf die der Image-Server zugreifen kann.

## Einschränkungen {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Ausländische Bildquellen werden nicht durch den Standard-Bildmechanismus abgedeckt. Wenn eine ausländische Bildquelle nicht gültig ist, wird ein Fehler zurückgegeben.

## Standard {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Vererbt von `default::DefaultImage`, wenn nicht definiert. Wenn definiert, aber leer, ist das Standardbildverhalten deaktiviert, auch wenn `default::DefaultImage` definiert ist.

## Verwandte Themen {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
