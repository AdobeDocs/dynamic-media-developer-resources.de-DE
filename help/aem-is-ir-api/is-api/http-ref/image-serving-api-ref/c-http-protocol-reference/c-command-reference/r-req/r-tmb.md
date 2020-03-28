---
description: Miniaturbild. Fordert Bilddaten an, die mithilfe von Katalogminiaturkriterien formatiert und in der Größe angepasst wurden.
seo-description: Miniaturbild. Fordert Bilddaten an, die mithilfe von Katalogminiaturkriterien formatiert und in der Größe angepasst wurden.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# tmb{#tmb}

Miniaturbild. Fordert Bilddaten an, die mithilfe von Katalogminiaturkriterien formatiert und in der Größe angepasst wurden.

`req=tmb`

Das Antwortdatenformat und der AntwortmIME-Typ werden durch `fmt=`festgelegt. Unterstützt alle Befehle außer `fit=`.

Siehe [Miniaturansicht](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

Die HTTP-Antwort kann auf der Grundlage von `catalog::Expiration`TTL zwischengespeichert werden.
