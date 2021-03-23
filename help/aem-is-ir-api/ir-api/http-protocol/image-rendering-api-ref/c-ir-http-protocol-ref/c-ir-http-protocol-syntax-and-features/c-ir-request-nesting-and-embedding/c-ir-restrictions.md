---
description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
seo-description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
seo-title: Einschränkungen
solution: Experience Manager
title: Einschränkungen
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Beschränkungen{#restrictions}

Für das Verschachteln und Einbetten gelten einige Einschränkungen.

Für eine gute Serverleistung sollte die Auflösung der von verschachtelten Anforderungen zurückgegebenen Bilder der Texturauflösung des Objekts/der Objekte, auf das/die das Material angewendet wird, angemessen entsprechen.

Ausländische Bilder werden lokal zwischengespeichert. Änderungen an solchen Bildern werden erst erkannt, nachdem der lokale Cache-Eintrag statisch ist (basierend auf dem HTTP-Header expires).
