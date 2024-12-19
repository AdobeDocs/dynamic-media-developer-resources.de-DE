---
title: Asset-Zusammenfassung
description: Metadaten-Suchergebnisse, die zusammengefasste Informationen zu einem Asset enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 10%

---

# [!DNL AssetSummary]{#assetsummary}

Metadaten-Suchergebnisse, die zusammengefasste Informationen zu einem Asset enthalten.

Syntax

## Parameter {#section-ebc75cc024d94c439260d2e71873cc74}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Asset-Handle. |
| Typ | `xsd:string` | Asset-Typ Die Konstante „Asset-Typen“ definiert die möglichen Werte. Optional. |
| name | `xsd:string` | Asset-Name. Optional. |
| Ordner | `xsd:string` | Der Ordner, der das Asset enthält. |
| Dateiname | `xsd:string` | Dateiname des Assets. |
| erstellt | `xsd:dateTime` | Asset-Erstellungsdatum. |
| createUser | `xsd:string` | Der Benutzer, der das Asset erstellt hat. |
| lastModify | `xsd:dateTime` | Das Datum der letzten Aktualisierung des Assets. |
| lastModifyUser | `xsd:string` | Der letzte Benutzer, der das Asset geändert hat. |
| metadataArray | `types:MetadataArray` | Ein Array von Metadatenwerten, die mit dem Asset verknüpft sind. |
| Punktstand | `xsd:double` | Bestimmt die Präzision bei einer Ähnlichkeitssuche (0 = keine Übereinstimmung, 1 = exakte Übereinstimmung). |
| scoreDetail | `xsd:string` | Es enthält detaillierte Informationen über ähnliche Bereiche infolge einer Ähnlichkeitssuche. |
