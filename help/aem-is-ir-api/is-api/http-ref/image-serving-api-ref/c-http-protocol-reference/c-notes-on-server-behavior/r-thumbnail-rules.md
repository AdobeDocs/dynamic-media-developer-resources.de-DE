---
description: Beachten Sie diese Regeln für Miniaturansichten.
solution: Experience Manager
title: Regeln für Miniaturen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Regeln für Miniaturen{#thumbnail-rules}

Beachten Sie diese Regeln für Miniaturansichten.

1. Wenn `catalog::ThumbType=Crop`, wird das (zugeschnittene) Bild auf die kleinstmögliche Größe skaliert, während gleichzeitig der gesamte Zielrect abgedeckt wird. Wenn `catalog::ThumbType=Fit`, wird das (zugeschnittene) Bild auf die größtmögliche Größe skaliert, wobei das gesamte Bild dennoch in den Zielrect passt. Wenn `catalog::ThumbType=Texture`, wird das (zugeschnittene) Bild auf das Verhältnis von `catalog::ThumbRes` zu `catalog::Resolution` skaliert.
1. Richten Sie das skalierte Bild basierend auf `attribute::ThumbHorizAlign` und `attribute::ThumbVertAlign` mit dem Ziel-Rect aus.
1. Zuschneiden des Ergebnisses auf das Zielrect.
