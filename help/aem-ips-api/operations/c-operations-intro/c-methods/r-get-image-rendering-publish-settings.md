---
description: Nur zur internen Verwendung. Siehe den Abschnitt Katalogreferenz-Katalogattribute für das Rendern von Bildern.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Nur zur internen Verwendung. Siehe den Abschnitt Katalogreferenz-Katalogattribute für das Rendern von Bildern.

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
| companyHandle | `xsd:string` | Ja | Der Handler für das Unternehmen, dessen Image-Rendering-Veröffentlichungseinstellungen Sie erhalten möchten. |
| contextHandle | `xsd:string` | Ja | Verarbeiten Sie den Veröffentlichungskontext. |

**Ausgabe (getImageRenderingPublishSettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | Ja | Veröffentlichungseinstellungen für das Rendern von Bildern. |
