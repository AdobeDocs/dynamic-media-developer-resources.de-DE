---
title: Asset-Zusammenfassung
description: Metadaten-Suchergebnisse, die zusammengefasste Informationen zu einem Asset enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
TQID: 'https://experienceleague.adobe.com/RHT8NJiS0pGKUcrYGBsSI1vewvRGUCZmsPYP6Pb0OBs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 125
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

