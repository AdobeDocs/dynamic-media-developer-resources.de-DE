---
description: Fügt einem Asset Viewer-Konfigurationseinstellungen hinzu. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 12%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Fügt einem Asset Viewer-Konfigurationseinstellungen hinzu. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.

Syntax

## Autorisierte Benutzertypen {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-bcc8c83cc84141e8b1341be9133e8511}

**Input (setViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| name | `xsd:string` | Ja | Asset-Name. |
| Typ | `xsd:string` | Ja | Der Typ des Assets, auf das Sie die Viewer-Konfiguration anwenden möchten. |
| configSettingArray | `types:ConfigSettingArray` | Ja | Das Array von `ConfigSettings`, die auf das Asset angewendet wurden. |

**Ausgabe (setViewerConfigSettingsParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

