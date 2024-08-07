---
title: TrustedDomains
description: Webdomänen der Flash-Anwendung. Adobe Flash-Anwendungen benötigen möglicherweise Zugriff auf die Eigenschaften von Bildern, die im swf-Format bereitgestellt werden. Der swf muss den Zugriff explizit gewähren, indem er den Namen der Anwendungsdomänen registriert, denen er vertraut.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Webdomänen der Flash-Anwendung. Adobe Flash-Anwendungen benötigen möglicherweise Zugriff auf die Eigenschaften von Bildern, die im swf-Format bereitgestellt werden. Der swf muss den Zugriff explizit gewähren, indem er den Namen der Anwendungsdomänen registriert, denen er vertraut.

## Eigenschaften {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Zeichenfolge, die eine kommagetrennte Liste mit Webdomänennamen enthält. Wenn dieses Feld leer ist, müssen Anwendungen von derselben Domäne wie das Bild-Rendering bereitgestellt werden, damit sie auf die Eigenschaften von Bildern in im [!DNL swf]-Format formatierten Antworten zugreifen können.

## Standard {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Wird von `default::TrustedDomains` vererbt, falls nicht vorhanden.

## Verwandte Themen {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
