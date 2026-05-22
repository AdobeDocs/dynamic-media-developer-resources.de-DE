---
title: Unterschiedliche Trübung des Materials
description: Die variable Deckkraft wird für Volltonfarben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Abziehbilder und Fensterabdeckungsmaterialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# Unterschiedliche Trübung des Materials{#varying-material-opacity}

Die variable Deckkraft wird für Volltonfarben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Abziehbilder und Fensterabdeckungsmaterialien.

Opazitätsinformationen können einfach mithilfe eines RGB-Bildes mit einem Alphakanal bereitgestellt werden. Darüber hinaus kann die Gesamtdeckkraft mit dem Befehl `opacity=` variiert werden (sowohl für RGB- als auch für RGBA-Bilder).

Wandränder unterstützen auch RGBA-Bilder, vor allem um gestanzte Ränder zu unterstützen.

Die [!DNL vnw] Dateien, die Fensterabdeckungen definieren, können einen Opazitätskanal enthalten. Es wird vom Renderer mit dem Alphakanal der wiederholbaren Textur und dem `opacity=` Wert kombiniert, um eine vollständige Palette von Deckkrafteffekten für schiere und durchsichtige Fensterbehandlungen zu bieten.
