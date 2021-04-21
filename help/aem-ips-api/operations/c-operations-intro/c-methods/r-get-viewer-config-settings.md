---
description: Ruft alle mit dem angegebenen Asset verknüpften Viewer-Konfigurationseinstellungen ab.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getViewerConfigSettings{#getviewerconfigsettings}

Ruft alle mit dem angegebenen Asset verknüpften Viewer-Konfigurationseinstellungen ab.

Syntax

## Autorisierte Benutzertypen {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Input (getViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Asset. |

**Output (getViewerCoinfigSettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Ja | Viewer-Typ, auf den die Konfigurationseinstellungen angewendet werden. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Ja | Array von Viewer-Konfigurationseinstellungen. |

