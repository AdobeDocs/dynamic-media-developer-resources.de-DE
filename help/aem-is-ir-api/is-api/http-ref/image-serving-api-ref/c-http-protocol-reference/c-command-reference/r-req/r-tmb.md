---
description: Miniaturbild. Fordert Bilddaten an, die mithilfe von Katalogminiaturkriterien formatiert und in der Größe angepasst wurden.
seo-description: Miniaturbild. Fordert Bilddaten an, die mithilfe von Katalogminiaturkriterien formatiert und in der Größe angepasst wurden.
seo-title: tmb
solution: Experience Manager
title: tmb
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# tmb{#tmb}

Miniaturbild. Fordert Bilddaten an, die mithilfe von Katalogminiaturkriterien formatiert und in der Größe angepasst wurden.

`req=tmb`

Das Antwortdatenformat und der AntwortmIME-Typ werden von `fmt=` bestimmt. Unterstützt alle Befehle mit Ausnahme von `fit=`.

Siehe [Skalierung der Miniaturansichten](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

Die HTTP-Antwort kann mit der TTL auf der Grundlage von `catalog::Expiration` zwischengespeichert werden.
