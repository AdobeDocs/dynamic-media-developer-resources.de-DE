---
description: Hält einen derzeit ausgeführten Auftrag an.
seo-description: Hält einen derzeit ausgeführten Auftrag an.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Scene7 Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# stopJob{#stopjob}

Hält einen derzeit ausgeführten Auftrag an.

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

**Input (stopJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`jobHandle`*` | `xsd:string` | Ja | Behandeln Sie den Auftrag, den Sie beenden möchten. |

**Output (stopJobReturn0**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Anforderung**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Antwort**

Keine.
