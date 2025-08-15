---
title: Unterschiedliche Trübung des Materials
description: Die variable Deckkraft wird für Volltonfarben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Abziehbilder und Fensterabdeckungsmaterialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Unterschiedliche Trübung des Materials{#varying-material-opacity}

Die variable Deckkraft wird für Volltonfarben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Abziehbilder und Fensterabdeckungsmaterialien.

Opazitätsinformationen können einfach mithilfe eines RGB-Bildes mit einem Alphakanal bereitgestellt werden. Darüber hinaus kann die Gesamtdeckkraft mit dem Befehl `opacity=` variiert werden (sowohl für RGB- als auch für RGBA-Bilder).

Wandränder unterstützen auch RGBA-Bilder, vor allem um gestanzte Ränder zu unterstützen.

Die [!DNL vnw] Dateien, die Fensterabdeckungen definieren, können einen Opazitätskanal enthalten. Es wird vom Renderer mit dem Alphakanal der wiederholbaren Textur und dem `opacity=` Wert kombiniert, um eine vollständige Palette von Deckkrafteffekten für schiere und durchsichtige Fensterbehandlungen zu bieten.
