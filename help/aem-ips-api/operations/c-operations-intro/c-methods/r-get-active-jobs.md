---
description: Ruft alle derzeit aktiven Aufträge ab.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 14%

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

**Eingabe (getActiveJobsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Nein | Der Griff zum Unternehmen. |
| jobHandle | `xsd:string` | Nein | Der Handler für den Auftrag. |
| originalName | `xsd:string` | Nein | Ursprünglicher Auftragsname. |

**Ausgabe (getActiveJobsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| jobArray | `xsd:string` | Ja | Array aktiver Aufträge. |

## Beispiele {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Dieses Codebeispiel gibt alle aktiven Aufträge eines Unternehmens zurück, das in IPS ausgeführt wird. In diesem Fall ist die Antwort ungewöhnlich, da der IPS-Planungskoordinator deaktiviert ist und keine aktiven Aufträge ausgeführt werden. Unter normalen Umständen würde die Antwort eine Reihe aktiver Aufträge zurückgeben.

**Anfrage**

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
