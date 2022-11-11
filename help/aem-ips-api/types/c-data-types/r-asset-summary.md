---
description: Metadaten-Suchergebnisse, die zusammengefasste Informationen über ein Asset enthalten.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

Metadaten-Suchergebnisse, die zusammengefasste Informationen über ein Asset enthalten.

Syntax

## Parameter {#section-ebc75cc024d94c439260d2e71873cc74}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Asset-Handle. |
| Typ | `xsd:string` | Asset-Typ. Die Konstante &quot;Asset-Typen&quot;definiert die möglichen Werte. Optional. |
| name | `xsd:string` | Asset-Name. Optional. |
| Ordner | `xsd:string` | Der Ordner, der das Asset enthält. |
| Dateiname | `xsd:string` | Dateiname des Assets. |
| erstellt | `xsd:dateTime` | Erstellungsdatum des Assets. |
| createUser | `xsd:string` | Der Benutzer, der das Asset erstellt hat. |
| lastModified | `xsd:dateTime` | Das Datum, an dem das Asset zuletzt aktualisiert wurde. |
| lastModifyUser | `xsd:string` | Der letzte Benutzer, der das Asset geändert hat. |
| metadataArray | `types:MetadataArray` | Array von Metadatenwerten, die mit dem Asset verknüpft sind. |
| Punktstand | `xsd:double` | Definiert die Genauigkeit im Fall einer Ähnlichkeitssuche (0 = keine Übereinstimmung, 1 = genaue Übereinstimmung). |
| scoreDetail | `xsd:string` | Enthält detaillierte Informationen zu ähnlichen Bereichen als Ergebnis einer Ähnlichkeitssuche. |
