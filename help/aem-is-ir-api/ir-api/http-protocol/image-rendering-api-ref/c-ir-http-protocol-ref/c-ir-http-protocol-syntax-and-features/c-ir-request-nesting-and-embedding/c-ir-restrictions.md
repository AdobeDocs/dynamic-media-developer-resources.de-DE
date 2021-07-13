---
description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
solution: Experience Manager
title: Einschränkungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Einschränkungen{#restrictions}

Für das Verschachteln und Einbetten gelten einige Einschränkungen.

Für eine gute Server-Leistung sollte die Auflösung der von verschachtelten Anforderungen zurückgegebenen Bilder in angemessener Weise mit der Texturauflösung der Objekte übereinstimmen, auf die das Material angewendet wird.

Ausländische Bilder werden lokal zwischengespeichert. Änderungen an solchen Bildern werden erst erkannt, nachdem der lokale Cache-Eintrag veraltet ist (basierend auf dem ablaufenden HTTP-Header).
