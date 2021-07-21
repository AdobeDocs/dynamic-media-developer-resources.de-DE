---
description: Löscht einen aktuellen oder geplanten Auftrag.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

---

# deleteJob{#deletejob}

Löscht einen aktuellen oder geplanten Auftrag.

Syntax

## Autorisierte Benutzertypen {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Eingabe (deleteJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle des Unternehmens, zu dem der Auftrag gehört. |
| `*`jobHandle`*` | `xsd:string` | Ja | Der Handle für den zu löschenden Auftrag. |

**Ausgabe**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Mit diesem Codebeispiel wird ein Auftrag gelöscht, der in IPS ausgeführt wird oder ausgeführt werden soll. Dazu ist ein Auftrags-Handle erforderlich, das Sie von einem anderen Vorgang erhalten müssen.

**Anforderung**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Antwort**

Keine.
