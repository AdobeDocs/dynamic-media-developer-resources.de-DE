---
description: Ruft alle derzeit aktiven Aufträge ab.
seo-description: Ruft alle derzeit aktiven Aufträge ab.
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Scene7 Image Production System API
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActiveJobs{#getactivejobs}

Ruft alle derzeit aktiven Aufträge ab.

Syntax

## Autorisierte Benutzertypen {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Input (getActiveJobsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nein | Der Griff zur Firma. |
| ` *`jobHandle`*` | `xsd:string` | Nein | Der Griff zum Auftrag. |
| ` *`originalName`*` | `xsd:string` | Nein | Ursprünglicher Auftragsname. |

**Output (getActiveJobsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`jobArray`*` | `xsd:string` | Ja | Array aktiver Aufträge. |

## Beispiele {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Dieses Codebeispiel gibt alle aktiven Aufträge einer Firma zurück, die in IPS ausgeführt wird. In diesem Fall ist die Antwort ungewöhnlich, da der IPS-Planungskoordinator deaktiviert ist und keine aktiven Aufträge ausgeführt werden. Unter normalen Umständen würde die Antwort eine Reihe aktiver Aufträge zurückgeben.

**Anforderung**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Antwort**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```

