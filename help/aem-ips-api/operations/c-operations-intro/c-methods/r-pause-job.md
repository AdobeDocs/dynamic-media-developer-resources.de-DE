---
description: Hält einen aktiven Auftrag an.
seo-description: Hält einen aktiven Auftrag an.
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
topic: Scene7 Image Production System API
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

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

**Input (pauseJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| ` *`jobHandle`*` | `xsd:string` | Ja | Behandeln Sie den Auftrag, den Sie anhalten möchten. |

**Output (PauseJobReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-ee4914f9496f4bd88556728a48fb22c1}

Dieses Codebeispiel hält einen aktiven Auftrag an.

**Anforderung**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Antwort**

Keine.
