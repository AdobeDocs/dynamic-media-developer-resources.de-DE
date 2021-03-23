---
description: Ruft eine Liste aktiver Kontexte für die Veröffentlichung für die angegebene Firma ab. Ein Veröffentlichungskontext gilt als aktiv, wenn mindestens ein aktiver Server für den Kontext definiert ist.
seo-description: Ruft eine Liste aktiver Kontexte für die Veröffentlichung für die angegebene Firma ab. Ein Veröffentlichungskontext gilt als aktiv, wenn mindestens ein aktiver Server für den Kontext definiert ist.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 8%

---


# getActivePublishContext{#getactivepublishcontext}

Ruft eine Liste aktiver Kontexte für die Veröffentlichung für die angegebene Firma ab. Ein Veröffentlichungskontext gilt als aktiv, wenn mindestens ein aktiver Server für den Kontext definiert ist.

Syntax

## Autorisierte Benutzertypen {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-a4be4024e55c472fa6728faec9c5e048}

**Input (getActivePublishContextsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle für aktive Kontexte mit Veröffentlichung der Firma zur Abfrage |

**Output (getActivePublishContextsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | Ja | Das Array der aktiven Kontexte im Veröffentlichungsmodus, die null oder mehr Werte aus dem Veröffentlichungskontext enthalten können. |

