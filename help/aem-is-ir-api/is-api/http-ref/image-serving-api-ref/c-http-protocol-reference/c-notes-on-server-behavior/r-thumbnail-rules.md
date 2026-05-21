---
description: Beachten Sie diese Miniaturansichtsregeln.
solution: Experience Manager
title: Regeln für Miniaturansichten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# Regeln für Miniaturansichten{#thumbnail-rules}

Beachten Sie diese Miniaturansichtsregeln.

1. Wenn `catalog::ThumbType=Crop`, wird das (zugeschnittene) Bild auf die kleinstmögliche Größe skaliert, während es weiterhin die gesamte Zielrect abdeckt. Wenn `catalog::ThumbType=Fit`, wird das (zugeschnittene) Bild auf die größtmögliche Größe skaliert, während das gesamte Bild noch in die Zielrect eingepasst wird. Wenn `catalog::ThumbType=Texture`, wird das (zugeschnittene) Bild auf das Verhältnis von `catalog::ThumbRes` zu `catalog::Resolution` skaliert.
1. Richten Sie das skalierte Bild basierend auf `attribute::ThumbHorizAlign` und `attribute::ThumbVertAlign` am Zielrect aus.
1. Beschneiden Sie das Ergebnis auf die Zielebene.
