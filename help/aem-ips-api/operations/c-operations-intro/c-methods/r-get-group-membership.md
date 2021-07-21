---
description: Gibt die Mitglieder einer Gruppe zurück.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

---

# getGroupMembership{#getgroupmembership}

Gibt die Mitglieder einer Gruppe zurück.

Syntax

## Autorisierte Benutzertypen {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-2e92f850254e46e48403acaa215341a5}

**Eingabe (getGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nein | Der Handle für den Benutzer. |
| `*`companyHandle`*` | `xsd:string` | Nein | Der Handle für das Unternehmen. |

**Ausgabe (getGroupMembershipReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Ja | Array von Gruppen. |

## Beispiele {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Dieses Codebeispiel gibt alle Mitglieder einer Gruppe zurück. Da die Handles für Unternehmen und Benutzer optional sind, kann der Vorgang alle Mitglieder aller Gruppen zurückgeben.

**Anforderung**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Antwort**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
