---
title: Unterschiedliche Materialdeckkraft
description: Die variable Deckkraft wird für feste Farben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Decals und Materialien, die mit Fenstern versehen sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Unterschiedliche Materialdeckkraft{#varying-material-opacity}

Die variable Deckkraft wird für feste Farben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Decals und Materialien, die mit Fenstern versehen sind.

Informationen zur Deckkraft können einfach über ein RGB-Bild mit einem Alphakanal bereitgestellt werden. Darüber hinaus kann die Gesamtdeckkraft mit dem Befehl `opacity=` variieren (sowohl für RGB- als auch für RGBA-Bilder).

Pinnwände unterstützen auch RGBA-Bilder, vor allem zur Unterstützung von durchgeschnittenen Grenzen.

Die [!DNL vnw] -Dateien, die Fensterbeläge definieren, können einen Deckkraftkanal enthalten. Sie wird vom Renderer mit dem Alphakanal der wiederholbaren Textur und dem Wert `opacity=` kombiniert, um eine vollständige Palette von Deckkrafteffekten für schiere und durchsichtige Fensterbehandlungen zu erhalten.
