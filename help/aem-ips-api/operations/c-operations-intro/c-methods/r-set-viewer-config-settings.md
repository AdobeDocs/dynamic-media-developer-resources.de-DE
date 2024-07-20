---
description: Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

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
| companyHandle | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| name | `xsd:string` | Ja | Asset-Name. |
| Typ | `xsd:string` | Ja | Der Asset-Typ, auf den Sie die Viewer-Konfiguration anwenden möchten. |
| configSettingArray | `types:ConfigSettingArray` | Ja | Das Array von &quot;`ConfigSettings`&quot;, das auf das Asset angewendet wird. |

**Output (setViewerConfigSettingsParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
