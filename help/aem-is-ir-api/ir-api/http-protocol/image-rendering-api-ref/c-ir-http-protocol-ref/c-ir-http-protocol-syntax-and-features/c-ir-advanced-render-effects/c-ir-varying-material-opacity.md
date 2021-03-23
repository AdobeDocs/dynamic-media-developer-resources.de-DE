---
description: Die variable Deckkraft wird für einfarbige und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Dekore und Fensterbedeckungsmaterialien.
seo-description: Die variable Deckkraft wird für einfarbige und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Dekore und Fensterbedeckungsmaterialien.
seo-title: Unterschiedliche Materialdeckkraft
solution: Experience Manager
title: Unterschiedliche Materialdeckkraft
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Unterschiedliche Materialdeckkraft{#varying-material-opacity}

Die variable Deckkraft wird für einfarbige und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Dekore und Fensterbedeckungsmaterialien.

Informationen zur Deckkraft können einfach mit einem RGB-Kanal mit einem Alpha-Bild bereitgestellt werden. Darüber hinaus kann die Gesamtdeckkraft mit dem Befehl `opacity=` geändert werden (sowohl für RGB- als auch für RGBA-Bilder).

An den Wall-Rändern werden auch RGBA-Bilder unterstützt, vor allem zur Unterstützung von durchgestrichenen Rändern.

Die [!DNL vnw]-Dateien, die Fensterbeläge definieren, können einen Deckkraftwert-Kanal enthalten, der vom Renderer mit dem Alpha-Kanal der wiederholbaren Textur und dem `opacity=`-Wert kombiniert wird, um eine vollständige Palette von Deckkrafteffekten für schiere und durchsichtige Fensterbehandlungen zu bieten.
