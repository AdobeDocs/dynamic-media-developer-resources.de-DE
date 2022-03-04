---
title: Einschränkungen
description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Einschränkungen{#restrictions}

Für das Verschachteln und Einbetten gelten einige Einschränkungen.

Für eine gute Server-Leistung sollte die Auflösung der von verschachtelten Anforderungen zurückgegebenen Bilder der Texturauflösung der Objekte entsprechen, auf die das Material angewendet wird.

Ausländische Bilder werden lokal zwischengespeichert. Änderungen an diesen Bildern werden erst erkannt, nachdem der lokale Cache-Eintrag veraltet ist (basierend auf dem ablaufenden HTTP-Header).
