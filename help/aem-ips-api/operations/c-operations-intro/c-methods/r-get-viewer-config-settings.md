---
description: Ruft alle mit dem angegebenen Asset verknüpften Viewer-Konfigurationseinstellungen ab.
seo-description: Ruft alle mit dem angegebenen Asset verknüpften Viewer-Konfigurationseinstellungen ab.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 18%

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

