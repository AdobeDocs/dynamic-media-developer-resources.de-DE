---
description: Ruft Aufträge zur Ausführung ab.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getScheduledJobs{#getscheduledjobs}

Ruft Aufträge zur Ausführung ab.

Syntax

## Autorisierte Benutzertypen {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2af604ff8282460990b9237158187f8f}

**Eingabe (getScheduledJobsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen. |
| jobHandle | `xsd:string` | Nein | Auftragsverarbeitung. |
| originalName | `xsd:string` | Nein | Der von `submitJob` angegebene Name. |

**Ausgabe (getScheduledJobsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | Ja | Array geplanter Aufträge. |

## Beispiele {#section-e79e7da86ba848fd9996aa36de462e6c}

Dieses Codebeispiel gibt alle geplanten Aufträge in einem Auftrags-Array zurück. Das -Array selbst enthält detaillierte Informationen zu den Aufträgen.

**Anfrage**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Antwort**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```
