---
description: Nur zur internen Verwendung. Weitere Informationen finden Sie im Abschnitt Referenzkatalog zum Bild-Rendering-Material - Katalogattribute .
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Nur zur internen Verwendung. Weitere Informationen finden Sie im Abschnitt Referenzkatalog zum Bild-Rendering-Material - Katalogattribute .

Syntax

## Autorisierte Benutzertypen {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-4f2cb8c589384816bb2525654ec49963}

**Eingabe (getImageRenderingPublishSettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle für das Unternehmen, dessen Einstellungen zur Veröffentlichung von Bildern Sie erhalten möchten. |
| `*`contextHandle`*` | `xsd:string` | Ja | Umgang mit dem Veröffentlichungskontext. |

**Ausgabe (getImageRenderingPublishSettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Ja | Veröffentlichungseinstellungen für das Bild-Rendering. |
