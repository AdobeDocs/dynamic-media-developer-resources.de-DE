---
description: Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit dem TC-Verzeichnis angegeben wurde.
seo-description: Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit dem TC-Verzeichnis angegeben wurde.
seo-title: Serverprotokollierung
solution: Experience Manager
title: Serverprotokollierung
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3

---


# Serverprotokollierung{#server-logging}

Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit TC::directory angegeben wurde.

Protokolldateien werden in der Regel täglich erstellt und gedreht. Ältere Protokolldateien im Protokollordner werden nach einer bestimmten Anzahl von Tagen automatisch gelöscht ( `TC::maxDays`).

Wichtig Eine ausreichende Menge an Speicherplatz muss für Protokolldateien reserviert werden, damit nicht genügend Speicherplatz zur Verfügung steht. Bei stark verwendeten Server- und Standardprotokolleinstellungen ist unter Umständen ein Wert von 1-2 GB/Tag erforderlich.

Der Plattformserver und der Image-Server erstellen die drei unten beschriebenen Protokolldateitypen.

Andere Image Serving-Komponenten und bestimmte andere Scene7-Pakete, z. B. die Scene7-Viewer, können auch Protokolldateien im selben Ordner erstellen. Diese Protokolldateien dienen der internen Verwendung in Scene7 und können vom Scene7-Support zur Fehlerbehebung angefordert werden.

* [Zugriffsprotokoll](c-access-log.md)
* [Ablaufverfolgungsprotokoll](c-trace-log.md)
* [Image-Server-Protokoll](c-image-server-log.md)

## Verwandte Themen {#section-5ff5e46031b1461c92de24e632610d6d}

[Zugriffsprotokollierung](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Debug-/Ablaufverfolgungsprotokoll](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
