---
title: Vertrauenswürdige Domains
description: Flash von Anwendungs-Webdomains. Beim Adobe von Flash-Anwendungen muss möglicherweise auf die Eigenschaften von Bildern zugegriffen werden, die im SWF-Format bereitgestellt werden. Der SWF muss explizit Zugriff gewähren, indem er den Namen der vertrauenswürdigen Anwendungsdomänen registriert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# Vertrauenswürdige Domains{#trusteddomains}

Flash von Anwendungs-Webdomains. Beim Adobe von Flash-Anwendungen muss möglicherweise auf die Eigenschaften von Bildern zugegriffen werden, die im SWF-Format bereitgestellt werden. Der SWF muss explizit Zugriff gewähren, indem er den Namen der vertrauenswürdigen Anwendungsdomänen registriert.

## Eigenschaften {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Zeichenfolge, die eine kommagetrennte Liste von Web-Domain-Namen enthält. Wenn leer, müssen Programme von derselben Domain wie das Bild-Rendering bereitgestellt werden, um in [!DNL swf]-formatierten Antworten auf die Eigenschaften von Bildern zugreifen zu können.

## Standard {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Von `default::TrustedDomains` übernommen, falls nicht vorhanden.

## Verwandte Themen {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
