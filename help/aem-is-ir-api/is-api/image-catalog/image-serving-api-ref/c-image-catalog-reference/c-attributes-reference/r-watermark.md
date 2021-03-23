---
description: Wasserzeichenauswahl. Gibt die Katalog-ID des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.
seo-description: Wasserzeichenauswahl. Gibt die Katalog-ID des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.
seo-title: Wasserzeichen
solution: Experience Manager
title: Wasserzeichen
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 5%

---


# Wasserzeichen{#watermark}

Wasserzeichenauswahl. Gibt den Katalog::Id des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.

Falls angegeben, wendet der Server das Wasserzeichen auf die angeforderten Bilddaten für alle Bildanforderungen ( `req=img`) an.

## Eigenschaften {#section-fad6ffff4c5f4b5c8010281bc1377055}

Textzeichenfolge. Wenn angegeben, muss ein gültiger `Catalog::Id`-Wert in diesem Bildkatalog (oder im Standardkatalog, falls unter [!DNL default.ini] angegeben) sein.

## Standard {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Vererbt von `default::Watermark`, wenn nicht definiert. Wenn definiert, aber leer, wird für diesen Bildkatalog kein Wasserzeichen angewendet, auch wenn `default::Watermark` definiert ist.

## Verwandte Themen {#section-f15dbe31013849828d78588742dde58e}

[Katalog::ID](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
