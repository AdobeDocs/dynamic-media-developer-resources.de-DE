---
description: Achten Sie auf diese Miniaturregeln.
solution: Experience Manager
title: Miniaturansichtsregeln
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Miniaturansichtsregeln{#thumbnail-rules}

Achten Sie auf diese Miniaturregeln.

1. Wenn `catalog::ThumbType=Crop`, wird das (zugeschnittene) Bild auf die kleinstmögliche Größe skaliert, während gleichzeitig die gesamte Zielgruppe rect abgedeckt wird. Wenn `catalog::ThumbType=Fit`, wird das (zugeschnittene) Bild auf die größtmögliche Größe skaliert, während das gesamte Bild trotzdem in den Zielgruppe rect passt. Wenn `catalog::ThumbType=Texture`, wird das (zugeschnittene) Bild auf das Verhältnis von `catalog::ThumbRes` zu `catalog::Resolution` skaliert.
1. Richten Sie das skalierte Zielgruppe basierend auf `attribute::ThumbHorizAlign` und `attribute::ThumbVertAlign` an dem Rechteck aus.
1. Schneiden Sie das Ergebnis auf den Zielgruppen-Rect.

