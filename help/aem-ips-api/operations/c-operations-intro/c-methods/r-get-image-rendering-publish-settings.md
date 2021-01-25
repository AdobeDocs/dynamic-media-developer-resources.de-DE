---
description: Nur zur internen Verwendung. Siehe Abschnitt zu Katalogattributen für Bildwiedergabe-Material.
seo-description: Nur zur internen Verwendung. Siehe Abschnitt zu Katalogattributen für Bildwiedergabe-Material.
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Dynamic Media Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 14%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Nur zur internen Verwendung. Siehe Abschnitt zu Katalogattributen für Bildwiedergabe-Material.

Syntax

## Autorisierte Benutzertypen {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-4f2cb8c589384816bb2525654ec49963}

**Input (getImageRenderingPublishSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, deren Veröffentlichungseinstellungen für das Rendern von Bildern Sie erhalten möchten. |
| `*`contextHandle`*` | `xsd:string` | Ja | Behandeln Sie den Veröffentlichungskontext. |

**Output (getImageRenderingPublishSettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Ja | Einstellungen für das Rendern von Bildern. |

