---
description: Nur zur internen Verwendung. Die Benutzer sollten auf den Abschnitt Image Serving Image Catalog Reference - Attribute Reference verweisen.
seo-description: Nur zur internen Verwendung. Die Benutzer sollten auf den Abschnitt Image Serving Image Catalog Reference - Attribute Reference verweisen.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Dynamic Media Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Nur zur internen Verwendung. Die Benutzer sollten auf den Abschnitt Image Serving Image Catalog Reference - Attribute Reference verweisen.

Syntax

## Autorisierte Benutzertypen {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-79f0d54acd604ad2a5c96679334f2424}

**Input (getImageServingPublishSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit dem Image für Veröffentlichungseinstellungen. |
| `*`contextHandle`*` | `xsd:string` | Ja | Behandeln Sie den Veröffentlichungskontext. |

**Ausgabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Ja | Array von Veröffentlichungseinstellungen für den Image-Server. |

