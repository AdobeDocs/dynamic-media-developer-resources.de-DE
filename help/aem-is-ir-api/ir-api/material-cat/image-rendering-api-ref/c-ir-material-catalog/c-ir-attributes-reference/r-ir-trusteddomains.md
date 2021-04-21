---
description: Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen unter Umständen Zugriff auf die Eigenschaften von Bildern, die im SWF-Format bereitgestellt werden. Die SWF muss explizit Zugriff gewähren, indem sie den Namen der Anwendungsdomäne(n) registriert, denen sie vertraut.
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# TrustedDomains *{#trusteddomains}

Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen unter Umständen Zugriff auf die Eigenschaften von Bildern, die im SWF-Format bereitgestellt werden. Die SWF muss explizit Zugriff gewähren, indem sie den Namen der Anwendungsdomäne(n) registriert, denen sie vertraut.

## Eigenschaften {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Zeichenfolge, die eine kommagetrennte Liste von Webdomänennamen enthält. Wenn diese Variable leer ist, müssen Anwendungen von derselben Domäne wie das Image Rendering bereitgestellt werden, damit sie auf die Eigenschaften von Bildern in [!DNL swf]-formatierten Antworten zugreifen können.

## Standard {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Vererbt von `default::TrustedDomains`, wenn nicht vorhanden.

## Verwandte Themen {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
