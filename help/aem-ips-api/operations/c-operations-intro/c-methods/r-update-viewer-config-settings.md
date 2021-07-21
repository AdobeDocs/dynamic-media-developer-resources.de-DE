---
description: Aktualisiert die SWF-Viewer-Konfigurationseinstellungen.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer-Vorgaben
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

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

**Eingabe (updateViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Array von Konfigurationseinstellungen, die Sie auf den Viewer anwenden möchten. |

**Ausgabe (updateViewerConfigSettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
