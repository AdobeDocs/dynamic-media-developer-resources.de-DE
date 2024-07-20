---
description: Wasserzeichenauswahl. Gibt die Katalogkennung des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.
solution: Experience Manager
title: Wasserzeichen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# Wasserzeichen{#watermark}

Wasserzeichenauswahl. Gibt den Katalog::Id des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.

Falls angegeben, wendet der Server das Wasserzeichen auf die angeforderten Bilddaten für alle Bildanforderungen ( `req=img`) an.

## Eigenschaften {#section-fad6ffff4c5f4b5c8010281bc1377055}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `Catalog::Id` -Wert in diesem Bildkatalog (oder im Standardkatalog, falls in [!DNL default.ini] angegeben) sein.

## Standard {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Wird von `default::Watermark` übernommen, falls nicht definiert. Wenn definiert, aber leer, wird für diesen Bildkatalog kein Wasserzeichen angewendet, selbst wenn `default::Watermark` definiert ist.

## Verwandte Themen {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
