---
description: Startet einen angehaltenen Auftrag neu.
seo-description: Startet einen angehaltenen Auftrag neu.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
topic: Scene7 Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit dem Auftrag, den Sie neu starten möchten. |
| ` *`jobHandle`*` | `xsd:string` | Ja | Der Griff zum angehaltenen Auftrag. |

**Output (resumeJobReturn)**

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
