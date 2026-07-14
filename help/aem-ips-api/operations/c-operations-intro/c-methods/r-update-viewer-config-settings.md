---
description: Aktualisiert die SWF Viewer-Konfigurationseinstellungen.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
TQID: 'https://experienceleague.adobe.com/YcfK5U6MKvmV2ulOQ3s2sOOBsgASSeslCIrk87xLAv8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Aktualisiert die SWF Viewer-Konfigurationseinstellungen.

Syntax

## Autorisierte Benutzertypen {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-29790d933fb24aa392d0cb2d52d1310f}

**Eingabe (updateViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| configSettingArray | `types:ConfigSettingArray` | Ja | Array von Konfigurationseinstellungen, die auf den Viewer angewendet werden sollen. |

**Ausgabe (updateViewerConfigSettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

