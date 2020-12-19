---
description: Aktualisiert die Konfigurationseinstellungen des SWF-Viewers.
seo-description: Aktualisiert die Konfigurationseinstellungen des SWF-Viewers.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '65'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Array von Konfigurationseinstellungen, die Sie auf den Viewer anwenden möchten. |

**Output (updateViewerConfigSettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
