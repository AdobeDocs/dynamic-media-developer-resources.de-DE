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

---


# Miniaturansichtsregeln{#thumbnail-rules}

Achten Sie auf diese Miniaturregeln.

1. Wenn `catalog::ThumbType=Crop`dies der Fall ist, wird das (zugeschnittene) Bild auf die kleinstmögliche Größe skaliert, während gleichzeitig die gesamte Zielgruppe rect abgedeckt wird. Ist dies `catalog::ThumbType=Fit`der Fall, wird das Bild (zugeschnitten) auf die größtmögliche Größe skaliert, wobei das gesamte Bild trotzdem in den Zielgruppe rect passt. Wenn `catalog::ThumbType=Texture`das Bild (zugeschnitten) auf das Verhältnis von `catalog::ThumbRes` zu `catalog::Resolution`skaliert wird.
1. Richten Sie das skalierte Bild basierend auf `attribute::ThumbHorizAlign` und mit dem Zielgruppe-Rect aus `attribute::ThumbVertAlign`.
1. Schneiden Sie das Ergebnis auf den Zielgruppen-Rect.

