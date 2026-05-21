---
description: Bildgröße. Pixelgröße des Bildes mit voller Auflösung, auf das vom Katalogpfad verwiesen wird.
solution: Experience Manager
title: Größe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: 'https://experienceleague.adobe.com/wS28XEIvINBBoYZSI-frpSbCikCyC5AhT6TyDgMsGFg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 5%

---

# Größe{#size}

Bildgröße. Pixelgröße des Bildes mit voller Auflösung, auf das von catalog:path verwiesen wird.

Wenn dieser Wert angegeben ist, verwendet Image Serving ihn, um zu vermeiden, dass das Bild geöffnet werden muss, um die tatsächliche Bildgröße zu erhalten.

>[!NOTE]
>
>Wenn `catalog::Size`bereitgestellt wird und nicht mit der tatsächlichen Bildgröße mit voller Auflösung übereinstimmt, kann es zu undefiniertem Verhalten kommen.

## Eigenschaften {#section-5c914ec8b1444a8e99d811b647cd42a3}

Zwei ganze Zahlen, jeweils größer als 0, getrennt durch ein Komma. Optional.

## Standard {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Wenn das Feld nicht vorhanden oder leer ist, wird die tatsächliche Größe des Bildes verwendet.

## Verwandte Themen {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
