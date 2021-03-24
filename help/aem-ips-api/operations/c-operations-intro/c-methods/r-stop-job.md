---
description: Hält einen derzeit ausgeführten Auftrag an.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| `*`jobHandle`*` | `xsd:string` | Ja | Behandeln Sie den Auftrag, den Sie beenden möchten. |

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
