---
description: Die variable Deckkraft wird für feste Farben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Decals und Fensterabdeckungsmaterialien.
solution: Experience Manager
title: Unterschiedliche Materialdeckkraft
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Unterschiedliche Materialdeckkraft{#varying-material-opacity}

Die variable Deckkraft wird für feste Farben und wiederholbare Texturen unterstützt, die auf überlappende Objekte angewendet werden, sowie für Decals und Fensterabdeckungsmaterialien.

Informationen zur Deckkraft können einfach über ein RGB-Bild mit einem Alphakanal bereitgestellt werden. Darüber hinaus kann die Gesamtdeckkraft mit dem Befehl `opacity=` variieren (sowohl für RGB- als auch für RGBA-Bilder).

Pinnwände unterstützen auch RGBA-Bilder, vor allem zur Unterstützung von durchgeschnittenen Grenzen.

Die [!DNL vnw]-Dateien, die Fensterbeläge definieren, können einen Deckkraftkanal enthalten, der vom Renderer mit dem Alphakanal der wiederholbaren Textur und dem `opacity=`-Wert kombiniert wird, um eine vollständige Palette von Deckkrafteffekten für die Scher- und durchsichtige Fensterbearbeitung zu liefern.
