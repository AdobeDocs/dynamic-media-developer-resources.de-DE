---
description: Web-Domains von Flash-Anwendungen. Für Adobe Flash-Anwendungen ist möglicherweise der Zugriff auf die Eigenschaften von Bildern erforderlich, die mit fmt=swf oder fmt=swf3 bereitgestellt werden.
solution: Experience Manager
title: Vertrauenswürdige Domains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# Vertrauenswürdige Domains{#trusteddomains}

Web-Domains von Flash-Anwendungen. Für Adobe Flash-Anwendungen ist möglicherweise der Zugriff auf die Eigenschaften von Bildern erforderlich, die mit fmt=swf oder fmt=swf3 bereitgestellt werden.

Der SWF muss explizit Zugriff gewähren, indem er den Namen der vertrauenswürdigen Anwendungsdomänen registriert.

## Eigenschaften {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Zeichenfolge, die eine kommagetrennte Liste von Web-Domain-Namen enthält. Wenn leer, müssen Programme von derselben Domain wie das Bild-Rendering bereitgestellt werden, um in SWF-formatierten Antworten auf die Eigenschaften von Bildern zugreifen zu können.

## Standard {#section-5c52ed3c7310488380f5a6f9540bf981}

Von `default::TrustedDomains` übernommen, falls nicht vorhanden.

## Verwandte Themen {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
