---
description: Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
seo-description: Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 10%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| `*`name`*` | `xsd:string` | Ja | Asset-Name. |
| `*`type`*` | `xsd:string` | Ja | Der Asset-Typ, auf den Sie die Viewer-Konfiguration anwenden möchten. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Das Array von `ConfigSettings`, das auf das Asset angewendet wird. |

**Output (setViewerConfigSettingsParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
