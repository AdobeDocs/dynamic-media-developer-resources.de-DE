---
description: Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen unter Umständen Zugriff auf die Eigenschaften von Bildern, die im SWF-Format bereitgestellt werden. Die SWF muss explizit Zugriff gewähren, indem sie den Namen der Anwendungsdomäne(n) registriert, denen sie vertraut.
seo-description: Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen unter Umständen Zugriff auf die Eigenschaften von Bildern, die im SWF-Format bereitgestellt werden. Die SWF muss explizit Zugriff gewähren, indem sie den Namen der Anwendungsdomäne(n) registriert, denen sie vertraut.
seo-title: TrustedDomains *
solution: Experience Manager
title: TrustedDomains *
topic: Scene7 Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# TrustedDomains *{#trusteddomains}

Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen unter Umständen Zugriff auf die Eigenschaften von Bildern, die im SWF-Format bereitgestellt werden. Die SWF muss explizit Zugriff gewähren, indem sie den Namen der Anwendungsdomäne(n) registriert, denen sie vertraut.

## Eigenschaften {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Zeichenfolge, die eine kommagetrennte Liste von Webdomänennamen enthält. Wenn diese Variable leer ist, müssen Anwendungen von derselben Domäne wie das Image Rendering bereitgestellt werden, damit sie auf die Eigenschaften von Bildern in [!DNL swf]-formatierten Antworten zugreifen können.

## Standard {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Vererbt von `default::TrustedDomains`, wenn nicht vorhanden.

## Verwandte Themen {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
