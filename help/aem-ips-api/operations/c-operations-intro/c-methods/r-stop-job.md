---
description: Hält einen laufenden Auftrag an.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 18%

---

# stopJob{#stopjob}

Hält einen laufenden Auftrag an.

Syntax

## Autorisierte Benutzertypen {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2b64f074e37c4c38849994f3bc65342a}

**Eingabe (stopJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| jobHandle | `xsd:string` | Ja | Verarbeiten Sie den Auftrag, den Sie stoppen möchten. |

**Ausgabe (stopJobReturn0**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Anfrage**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Antwort**

Keine.
