---
description: Suchergebnisse für Metadaten, die zusammengefasste Informationen zu einem Asset enthalten.
seo-description: Suchergebnisse für Metadaten, die zusammengefasste Informationen zu einem Asset enthalten.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 10%

---


# AssetSummary{#assetsummary}

Suchergebnisse für Metadaten, die zusammengefasste Informationen zu einem Asset enthalten.

Syntax

## Parameter {#section-ebc75cc024d94c439260d2e71873cc74}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Asset-Handle. |
| `*`type`*` | `xsd:string` | Asset-Typ. Die Konstante &quot;Asset-Typen&quot;definiert die möglichen Werte. Optional. |
| `*`name`*` | `xsd:string` | Asset-Name. Optional. |
| `*`Ordner`*` | `xsd:string` | Der Ordner, der das Asset enthält. |
| `*`Dateiname`*` | `xsd:string` | Dateiname des Assets. |
| `*`erstellt`*` | `xsd:dateTime` | Erstellungsdatum des Assets |
| `*`createUser`*` | `xsd:string` | Der Benutzer, der das Asset erstellt hat. |
| `*`lastModified`*` | `xsd:dateTime` | Das Datum, an dem das Asset zuletzt aktualisiert wurde. |
| `*`lastModifyUser`*` | `xsd:string` | Der letzte Benutzer, der das Asset geändert hat. |
| `*`metadataArray`*` | `types:MetadataArray` | Array von Metadatenwerten, die mit dem Asset verknüpft sind. |
| `*`Punktstand`*` | `xsd:double` | Definiert die Genauigkeit bei einer Ähnlichkeitssuche (0 = keine Übereinstimmung, 1 = genaue Übereinstimmung). |
| `*`scoreDetail`*` | `xsd:string` | Enthält detaillierte Informationen zu ähnlichen Bereichen als Ergebnis einer Ähnlichkeitssuche. |

