---
description: Startet einen angehaltenen Auftrag neu.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 17%

---

# resumeJob{#resumejob}

Startet einen angehaltenen Auftrag neu.

Syntax

## Autorisierte Benutzertypen {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Eingabe (resumeJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen mit dem Auftrag, den Sie neu starten möchten. |
| jobHandle | `xsd:string` | Ja | Der Griff zum angehaltenen Auftrag. |

**Ausgabe (resumeJobReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d0524e031f1f43d89430eade19526162}

In diesem Codebeispiel wird ein angehaltener Auftrag neu gestartet.

**Anforderung**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Antwort**

Keine.
