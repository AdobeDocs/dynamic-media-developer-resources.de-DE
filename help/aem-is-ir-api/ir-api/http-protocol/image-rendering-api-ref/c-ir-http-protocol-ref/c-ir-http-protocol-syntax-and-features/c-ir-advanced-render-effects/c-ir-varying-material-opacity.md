---
description: Die variable Deckkraft wird für einfarbige und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Dekore und Fensterbedeckungsmaterialien.
seo-description: Die variable Deckkraft wird für einfarbige und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Dekore und Fensterbedeckungsmaterialien.
seo-title: Unterschiedliche Materialdeckkraft
solution: Experience Manager
title: Unterschiedliche Materialdeckkraft
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterschiedliche Materialdeckkraft{#varying-material-opacity}

Die variable Deckkraft wird für einfarbige und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Dekore und Fensterbedeckungsmaterialien.

Informationen zur Deckkraft können einfach mit einem RGB-Kanal mit einem Alpha-Bild bereitgestellt werden. Darüber hinaus kann die Gesamtdeckkraft mit dem `opacity=` Befehl variiert werden (sowohl für RGB- als auch für RGBA-Bilder).

An den Wall-Rändern werden auch RGBA-Bilder unterstützt, vor allem zur Unterstützung von durchgestrichenen Rändern.

Die [!DNL vnw] `opacity=` Dateien, die Fensterbeläge definieren, können einen Deckkraft-Kanal enthalten, der vom Renderer mit dem Alpha-Kanal der wiederholbaren Textur und dem Wert kombiniert wird, um eine vollständige Palette von Deckkraft-Effekten für schiere und durchsichtige Fensterbehandlungen bereitzustellen.
