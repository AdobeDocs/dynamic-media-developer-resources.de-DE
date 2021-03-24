---
description: Ruft alle derzeit aktiven Aufträge ab.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 15%

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
| `*`companyHandle`*` | `xsd:string` | Nein | Der Griff zur Firma. |
| `*`jobHandle`*` | `xsd:string` | Nein | Der Griff zum Auftrag. |
| `*`originalName`*` | `xsd:string` | Nein | Ursprünglicher Auftragsname. |

**Output (getActiveJobsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | Ja | Array aktiver Aufträge. |

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

