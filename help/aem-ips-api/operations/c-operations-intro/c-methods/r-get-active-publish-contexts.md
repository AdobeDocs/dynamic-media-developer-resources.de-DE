---
description: Ruft eine Liste der aktiven Veröffentlichungskontexte für das angegebene Unternehmen ab. Ein Veröffentlichungskontext wird als aktiv betrachtet, wenn mindestens ein aktiver Server für den Kontext definiert ist.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

Ruft eine Liste der aktiven Veröffentlichungskontexte für das angegebene Unternehmen ab. Ein Veröffentlichungskontext wird als aktiv betrachtet, wenn mindestens ein aktiver Server für den Kontext definiert ist.

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

**Eingabe (getActivePublishContextsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handler an das Unternehmen, um aktive Veröffentlichungskontexte abzufragen |

**Ausgabe (getActivePublishContextsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| contextArray | `types:StringArray` | Ja | Das Array aktiver Veröffentlichungskontexte, das null oder mehr Werte aus dem Veröffentlichungskontext enthalten kann. |
