---
description: Wasserzeichenselektor. Gibt die Katalog-ID des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.
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

Wasserzeichenselektor. Gibt den Katalog::ID des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.

Falls angegeben, wendet der Server das Wasserzeichen auf die angeforderten Bilddaten für alle Bildanforderungen an ( `req=img`).

## Eigenschaften {#section-fad6ffff4c5f4b5c8010281bc1377055}

Text-String Falls angegeben, muss ein gültiger `Catalog::Id` in diesem Bildkatalog (oder im Standardkatalog, falls in [!DNL default.ini] angegeben) sein.

## Standard {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Von `default::Watermark` geerbt, wenn nicht definiert. Wenn definiert, aber leer, wird für diesen Bildkatalog kein Wasserzeichen angewendet, auch wenn `default::Watermark` definiert ist.

## Verwandte Themen {#section-f15dbe31013849828d78588742dde58e}

[catalog:id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
