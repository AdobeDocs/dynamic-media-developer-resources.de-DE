---
description: Miniaturbild. Fordert Bilddaten an, die mithilfe der Kriterien für Katalogminiaturansichten formatiert und in der Größe angepasst wurden.
solution: Experience Manager
title: TMB
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# TMB{#tmb}

Miniaturbild. Fordert Bilddaten an, die mithilfe der Kriterien für Katalogminiaturansichten formatiert und in der Größe angepasst wurden.

`req=tmb`

Das Format der Antwortdaten und der MIME-Typ der Antwort werden durch `fmt=` bestimmt. Unterstützt alle Befehle außer `fit=`.

Siehe [Skalierung von Miniaturansichten](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.
