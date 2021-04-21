---
description: Für das Verschachteln und Einbetten gelten einige Einschränkungen.
solution: Experience Manager
title: Einschränkungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Beschränkungen{#restrictions}

Für das Verschachteln und Einbetten gelten einige Einschränkungen.

Für eine gute Serverleistung sollte die Auflösung der von verschachtelten Anforderungen zurückgegebenen Bilder der Texturauflösung des Objekts/der Objekte, auf das/die das Material angewendet wird, angemessen entsprechen.

Ausländische Bilder werden lokal zwischengespeichert. Änderungen an solchen Bildern werden erst erkannt, nachdem der lokale Cache-Eintrag statisch ist (basierend auf dem HTTP-Header expires).
