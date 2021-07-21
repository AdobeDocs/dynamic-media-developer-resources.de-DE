---
description: Fügt Viewer-Konfigurationseinstellungen an ein Asset an. Dabei kann es sich um eine Viewer-Vorgabe oder um das Quell-Asset für den Viewer handeln.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer-Vorgaben
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 11%

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

**Eingabe (setViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset-Handle. |
| `*`name`*` | `xsd:string` | Ja | Asset-Name. |
| `*`type`*` | `xsd:string` | Ja | Der Asset-Typ, auf den Sie die Viewer-Konfiguration anwenden möchten. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Das Array von `ConfigSettings`, das auf das Asset angewendet wird. |

**Ausgabe (setViewerConfigSettingsParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.
