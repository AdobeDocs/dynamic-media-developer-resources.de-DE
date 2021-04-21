---
description: Aktualisiert die Konfigurationseinstellungen des SWF-Viewers.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 13%

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

Aktualisiert die Konfigurationseinstellungen des SWF-Viewers.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Array von Konfigurationseinstellungen, die Sie auf den Viewer anwenden möchten. |

**Output (updateViewerConfigSettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
