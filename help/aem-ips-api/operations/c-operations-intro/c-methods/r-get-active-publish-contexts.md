---
description: Ruft eine Liste aktiver Kontexte für die Veröffentlichung für die angegebene Firma ab. Ein Veröffentlichungskontext gilt als aktiv, wenn mindestens ein aktiver Server für den Kontext definiert ist.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 10%

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
| `*`contextArray`*` | `types:StringArray` | Ja | Das Array der aktiven Kontexte für Veröffentlichungen, die null oder mehr Werte aus dem Veröffentlichungskontext enthalten können. |

