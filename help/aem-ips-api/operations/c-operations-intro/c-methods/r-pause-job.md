---
description: Hält einen aktiven Auftrag an.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

---

# pauseJob{#pausejob}

Hält einen aktiven Auftrag an.

Syntax

## Autorisierte Benutzertypen {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Eingabe (pauseJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| jobHandle | `xsd:string` | Ja | Führen Sie den Vorgang aus, den Sie anhalten möchten. |

**Ausgabe (PauseJobReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-ee4914f9496f4bd88556728a48fb22c1}

Dieses Codebeispiel setzt einen aktiven Auftrag aus.

**Anforderung**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Antwort**

Keine.
