---
description: Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit dem TC-Verzeichnis angegeben ist.
solution: Experience Manager
title: Serverprotokollierung
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# Serverprotokollierung{#server-logging}

Alle Protokolldateien werden in denselben Protokollordner geschrieben, der mit TC::directory angegeben wurde.

Protokolldateien werden in der Regel täglich erstellt und gedreht. Ältere Protokolldateien im Protokollordner werden nach einer bestimmten Anzahl von Tagen ( `TC::maxDays`) automatisch gelöscht.

Wichtig: Eine ausreichende Menge an Speicherplatz muss für Protokolldateien reserviert werden, damit nicht genügend Speicherplatz zur Verfügung steht. Für einen stark genutzten Server und die standardmäßigen Protokolleinstellungen sind möglicherweise 1-2 GB/Tag erforderlich.

Der Platform-Server und der Image-Server erstellen die drei unten beschriebenen Protokolldateitypen.

Andere Image Serving-Komponenten und bestimmte andere Dynamic Media-Pakete, wie z. B. die Dynamic Media-Viewer, können auch Protokolldateien im selben Ordner erstellen. Diese Protokolldateien sind für die interne Verwendung in Dynamic Media bestimmt und können vom technischen Support von Dynamic Media für Fehlerbehebungszwecke angefordert werden.

* [Zugriffsprotokoll](c-access-log.md)
* [Ablaufprotokoll](c-trace-log.md)
* [Image-Server-Protokoll](c-image-server-log.md)

## Verwandte Themen {#section-5ff5e46031b1461c92de24e632610d6d}

[Zugriffsprotokollierung](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f),  [Debug-/Ablaufprotokollierung](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
