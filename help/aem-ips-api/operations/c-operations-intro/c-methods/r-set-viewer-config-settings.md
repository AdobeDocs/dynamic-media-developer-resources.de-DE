---
description: Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
seo-description: Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
uuid: d83d866e-9243-479f-9b33-727aad8158e5
feature: Dynamic Media Classic,SDK/API,Viewer-Vorgaben
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

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
