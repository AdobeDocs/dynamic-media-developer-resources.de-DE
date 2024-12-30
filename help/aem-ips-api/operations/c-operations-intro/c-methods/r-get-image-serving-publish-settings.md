---
description: Nur zur internen Verwendung. Benutzer sollten den Abschnitt Image Serving Image Catalog Reference - Attribute Reference lesen.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Nur zur internen Verwendung. Benutzer sollten den Abschnitt Image Serving Image Catalog Reference - Attribute Reference lesen.

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
| companyHandle | `xsd:string` | Ja | Das -Handle an das Unternehmen mit den Image-Serving-Veröffentlichungseinstellungen. |
| contextHandle | `xsd:string` | Ja | Verarbeiten Sie den Veröffentlichungskontext. |

**Ausgabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| publishSettingArray | `xsd:string` | Ja | Array von Image-Server-Veröffentlichungseinstellungen. |
