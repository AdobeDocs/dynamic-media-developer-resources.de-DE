---
description: Flash von Anwendungs-Webdomains. Beim Adobe von Flash-Anwendungen muss möglicherweise auf die Eigenschaften der Bilder zugegriffen werden, die mit FMT=SWF oder FMT=SWF3 bereitgestellt werden.
solution: Experience Manager
title: Vertrauenswürdige Domains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# Vertrauenswürdige Domains{#trusteddomains}

Flash von Anwendungs-Webdomains. Beim Adobe von Flash-Anwendungen muss möglicherweise auf die Eigenschaften der Bilder zugegriffen werden, die mit FMT=SWF oder FMT=SWF3 bereitgestellt werden.

Der SWF muss explizit Zugriff gewähren, indem er den Namen der vertrauenswürdigen Anwendungsdomänen registriert.

## Eigenschaften {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Zeichenfolge, die eine kommagetrennte Liste von Web-Domain-Namen enthält. Wenn leer, müssen Programme von derselben Domain wie das Bild-Rendering bereitgestellt werden, um in SWF-formatierten Antworten auf die Eigenschaften von Bildern zugreifen zu können.

## Standard {#section-5c52ed3c7310488380f5a6f9540bf981}

Von `default::TrustedDomains` übernommen, falls nicht vorhanden.

## Verwandte Themen {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
