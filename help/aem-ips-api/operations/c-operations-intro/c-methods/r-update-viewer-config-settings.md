---
description: Aktualisiert die SWF-Viewer-Konfigurationseinstellungen.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Aktualisiert die SWF-Viewer-Konfigurationseinstellungen.

Syntax

## Autorisierte Benutzertypen {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-29790d933fb24aa392d0cb2d52d1310f}

**Input (updateViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| configSettingArray | `types:ConfigSettingArray` | Ja | Array von Konfigurationseinstellungen, die Sie auf den Viewer anwenden möchten. |

**Output (updateViewerConfigSettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
