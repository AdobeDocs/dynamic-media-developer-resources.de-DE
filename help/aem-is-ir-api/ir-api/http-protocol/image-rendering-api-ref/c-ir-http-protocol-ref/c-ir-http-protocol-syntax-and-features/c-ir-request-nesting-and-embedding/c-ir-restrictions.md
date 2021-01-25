---
description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
seo-description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
seo-title: Einschränkungen
solution: Experience Manager
title: Einschränkungen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Beschränkungen{#restrictions}

Für das Verschachteln und Einbetten gelten einige Einschränkungen.

Für eine gute Serverleistung sollte die Auflösung der von verschachtelten Anforderungen zurückgegebenen Bilder der Texturauflösung des Objekts/der Objekte, auf das/die das Material angewendet wird, angemessen entsprechen.

Ausländische Bilder werden lokal zwischengespeichert. Änderungen an solchen Bildern werden erst erkannt, nachdem der lokale Cache-Eintrag statisch ist (basierend auf dem HTTP-Header expires).
