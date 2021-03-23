---
description: Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit dem TC-Verzeichnis angegeben wurde.
solution: Experience Manager
title: Serverprotokollierung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# Serverprotokollierung{#server-logging}

Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit TC::directory angegeben wurde.

Protokolldateien werden in der Regel täglich erstellt und gedreht. Ältere Protokolldateien im Protokollordner werden nach einer bestimmten Anzahl von Tagen ( `TC::maxDays`) automatisch gelöscht.

Wichtig Eine ausreichende Menge an Speicherplatz muss für Protokolldateien reserviert werden, damit nicht genügend Speicherplatz zur Verfügung steht. Bei stark verwendeten Server- und Standardprotokolleinstellungen ist unter Umständen ein Wert von 1-2 GB/Tag erforderlich.

Der Plattformserver und der Image-Server erstellen die drei unten beschriebenen Protokolldateitypen.

Andere Image Serving-Komponenten und bestimmte andere Dynamic Media-Pakete, z. B. die Dynamic Media Viewer, können auch Protokolldateien im selben Ordner erstellen. Diese Protokolldateien sind für den internen Gebrauch von Dynamic Media bestimmt und können vom technischen Support von Dynamic Media für die Fehlerbehebung angefordert werden.

* [Zugriffsprotokoll](c-access-log.md)
* [Ablaufverfolgungsprotokoll](c-trace-log.md)
* [Image-Server-Protokoll](c-image-server-log.md)

## Verwandte Themen {#section-5ff5e46031b1461c92de24e632610d6d}

[Zugriffsprotokollierung](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f),  [Debug-/Ablaufverfolgungsprotokoll](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
