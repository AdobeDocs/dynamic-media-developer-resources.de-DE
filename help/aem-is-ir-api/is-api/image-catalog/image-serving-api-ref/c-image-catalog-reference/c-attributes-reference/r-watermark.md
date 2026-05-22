---
description: Wasserzeichenselektor. Gibt die Katalog-ID des Katalogdatensatzes an, der als Wasserzeichenbild oder Vorlage verwendet werden soll.
solution: Experience Manager
title: Wasserzeichen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
TQID: 'https://experienceleague.adobe.com/zajYc7BBw0BfJ6qvnTFiHY79quRa91-LdY3j1YynxVc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
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
