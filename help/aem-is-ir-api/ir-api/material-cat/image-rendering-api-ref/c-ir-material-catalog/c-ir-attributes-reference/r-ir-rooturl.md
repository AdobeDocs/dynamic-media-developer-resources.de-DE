---
title: RootUrl
description: Stamm-URL für relative Bild-URLs. Gibt die Stamm-URL für relative Bild-URLs an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# RootUrl{#rooturl}

Stamm-URL für relative Bild-URLs. Gibt die Stamm-URL für relative Bild-URLs an. Der `attribute::RootUrl` wird anstelle von `attribute::RootPath` verwendet, wenn ein `src=` von { geschweiften Klammern } eingeschlossen ist.

## Eigenschaften {#section-69cd0f71ea614770a8778c745d23197a}

Text-Zeichenfolgenwert. Absoluter URL-Stammpfad, einschließlich der führenden Protokollkennung. Die folgenden Protokolle werden unterstützt: HTTP, HTTPS und FTP.

## Standard {#section-7a81569728474725a70f3a2cc4d48e85}

Von `default::RootUrl` geerbt, wenn nicht definiert. Falls definiert, aber leer, werden relative URLs von diesem Materialkatalog nicht unterstützt.

## Verwandte Themen {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
