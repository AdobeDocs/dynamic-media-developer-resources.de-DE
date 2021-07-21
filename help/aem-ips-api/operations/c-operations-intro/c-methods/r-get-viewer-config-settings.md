---
description: Ruft alle mit dem angegebenen Asset verknüpften Viewer-Konfigurationseinstellungen ab.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer-Vorgaben
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

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

**Eingabe (getViewerConfigSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Asset. |

**Ausgabe (getViewerConfigSettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Ja | Viewer-Typ, auf den die Konfigurationseinstellungen angewendet werden. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Ja | Array von Viewer-Konfigurationseinstellungen. |
