---
description: Client-Cache-TTL für standardmäßige Bildantworten. Stellt das Ablaufintervall für Standardbildantworten bereit (Antworten, die ein Standardbild zurückgeben, das entweder mit defaultImage= oder mit defaultImage= festgelegt wurde).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
TQID: 'https://experienceleague.adobe.com/v-wtXCBtpHpf9mTjoQ58GZ9eXq-yR2tpGT0Kd-DTyNI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# DefaultExpiration{#defaultexpiration}

Client-Cache-TTL für standardmäßige Bildantworten. Stellt das Ablaufintervall für standardmäßige Bildantworten bereit (Antworten, die ein Standardbild zurückgeben, das entweder mit defaultImage= oder attribute::DefaultImage angegeben ist).

Wird nur angewendet, wenn das Standardbild nicht mit einem Katalogdatensatz verknüpft ist oder wenn der Standardbildkatalogdatensatz keinen bestimmten `catalog::Expiration` bereitstellt.

## Eigenschaften {#section-e564512476604fd7b964f9f2903d6d33}

Reelle Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf der Gültigkeit seit Generierung der Antwortdaten. Auf 0 gesetzt, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Client-Zwischenspeicherung für standardmäßige Bildantworten effektiv deaktiviert wird. Legen Sie die Einstellung auf `-1` fest, um als `never expire` zu markieren.

## Standard {#section-131cd32c2e214391857dba5af321f8cd}

Von `default::DefaultExpiration` geerbt, wenn nicht definiert oder leer.

TTL (Time-To-Live) ist die Dauer vor Ablauf des Cache. Die Standard-TTL ist 1 Stunde.

## Verwandte Themen {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
