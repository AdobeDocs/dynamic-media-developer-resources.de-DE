---
title: AssetSummary
description: Metadaten-Suchergebnisse, die zusammengefasste Informationen über ein Asset enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '123'
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
| Ordner | `xsd:string` | Der Ordner mit dem Asset. |
| Dateiname | `xsd:string` | Dateiname des Assets. |
| erstellt | `xsd:dateTime` | Erstellungsdatum des Assets. |
| createUser | `xsd:string` | Der Benutzer, der das Asset erstellt hat. |
| lastModified | `xsd:dateTime` | Das Datum der letzten Aktualisierung des Assets. |
| lastModifyUser | `xsd:string` | Der letzte Benutzer, der das Asset geändert hat. |
| metadataArray | `types:MetadataArray` | Ein Array von Metadatenwerten, die mit dem Asset verknüpft sind. |
| Punktstand | `xsd:double` | Definiert die Genauigkeit bei einer Ähnlichkeitssuche (0 = keine Übereinstimmung, 1 = genaue Übereinstimmung). |
| scoreDetail | `xsd:string` | Sie enthält detaillierte Informationen zu ähnlichen Bereichen als Ergebnis einer Ähnlichkeitssuche. |
