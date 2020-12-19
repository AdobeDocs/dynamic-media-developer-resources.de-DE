---
description: Achten Sie auf diese Miniaturregeln.
seo-description: Achten Sie auf diese Miniaturregeln.
seo-title: Miniaturansichtsregeln
solution: Experience Manager
title: Miniaturansichtsregeln
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Miniaturansichtsregeln{#thumbnail-rules}

Achten Sie auf diese Miniaturregeln.

1. Wenn `catalog::ThumbType=Crop`, wird das (zugeschnittene) Bild auf die kleinstmögliche Größe skaliert, während gleichzeitig die gesamte Zielgruppe rect abgedeckt wird. Wenn `catalog::ThumbType=Fit`, wird das (zugeschnittene) Bild auf die größtmögliche Größe skaliert, während das gesamte Bild trotzdem in den Zielgruppe rect passt. Wenn `catalog::ThumbType=Texture`, wird das (zugeschnittene) Bild auf das Verhältnis von `catalog::ThumbRes` zu `catalog::Resolution` skaliert.
1. Richten Sie das skalierte Zielgruppe basierend auf `attribute::ThumbHorizAlign` und `attribute::ThumbVertAlign` an dem Rechteck aus.
1. Schneiden Sie das Ergebnis auf den Zielgruppen-Rect.

