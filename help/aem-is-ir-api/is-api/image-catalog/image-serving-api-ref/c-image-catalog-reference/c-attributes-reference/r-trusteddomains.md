---
description: Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen möglicherweise Zugriff auf die Eigenschaften von Bildern, die mit "fmt=swf"oder "fmt=swf3"bereitgestellt werden.
seo-description: Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen möglicherweise Zugriff auf die Eigenschaften von Bildern, die mit "fmt=swf"oder "fmt=swf3"bereitgestellt werden.
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
topic: Scene7 Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# TrustedDomains{#trusteddomains}

Webdomänen für Flash-Anwendungen. Adobe Flash-Anwendungen benötigen möglicherweise Zugriff auf die Eigenschaften von Bildern, die mit &quot;fmt=swf&quot;oder &quot;fmt=swf3&quot;bereitgestellt werden.

Die SWF muss den Zugriff explizit gewähren, indem sie den Namen der Anwendungsdomänen registriert, denen sie vertrauen.

## Eigenschaften {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Zeichenfolge, die eine kommagetrennte Liste von Webdomänennamen enthält. Wenn diese Variable leer ist, müssen Anwendungen von derselben Domäne wie das Image Rendering bereitgestellt werden, damit sie auf die Eigenschaften von Bildern in SWF-formatierten Antworten zugreifen können.

## Standard {#section-5c52ed3c7310488380f5a6f9540bf981}

Vererbt von `default::TrustedDomains`, wenn nicht vorhanden.

## Verwandte Themen {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
