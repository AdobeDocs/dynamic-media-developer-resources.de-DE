---
description: Beachten Sie diese Miniaturansichtsregeln.
solution: Experience Manager
title: Regeln für Miniaturansichten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Regeln für Miniaturansichten{#thumbnail-rules}

Beachten Sie diese Miniaturansichtsregeln.

1. Wenn `catalog::ThumbType=Crop`, wird das (zugeschnittene) Bild auf die kleinstmögliche Größe skaliert, während es weiterhin die gesamte Zielrect abdeckt. Wenn `catalog::ThumbType=Fit`, wird das (zugeschnittene) Bild auf die größtmögliche Größe skaliert, während das gesamte Bild noch in die Zielrect eingepasst wird. Wenn `catalog::ThumbType=Texture`, wird das (zugeschnittene) Bild auf das Verhältnis von `catalog::ThumbRes` zu `catalog::Resolution` skaliert.
1. Richten Sie das skalierte Bild basierend auf `attribute::ThumbHorizAlign` und `attribute::ThumbVertAlign` am Zielrect aus.
1. Beschneiden Sie das Ergebnis auf die Zielebene.
