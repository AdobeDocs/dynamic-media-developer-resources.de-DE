---
description: Löscht einen aktuellen oder geplanten Auftrag.
seo-description: Löscht einen aktuellen oder geplanten Auftrag.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 11%

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

**Input (deleteJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, zu der der Auftrag gehört. |
| `*`jobHandle`*` | `xsd:string` | Ja | Das Handle zum zu löschenden Auftrag. |

**Ausgabe**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Dieses Codebeispiel löscht einen Auftrag, der in IPS ausgeführt wird oder ausgeführt werden soll. Es ist ein Auftragsgriff erforderlich, den Sie von einem anderen Vorgang abrufen müssen.

**Anforderung**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Antwort**

Keine.
