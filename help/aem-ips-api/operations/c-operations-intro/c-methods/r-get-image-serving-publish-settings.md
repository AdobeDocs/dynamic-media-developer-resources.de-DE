---
description: Nur zur internen Verwendung. Die Benutzer sollten auf den Abschnitt Image Serving Image Catalog Reference - Attribute Reference verweisen.
seo-description: Nur zur internen Verwendung. Die Benutzer sollten auf den Abschnitt Image Serving Image Catalog Reference - Attribute Reference verweisen.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 12%

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

