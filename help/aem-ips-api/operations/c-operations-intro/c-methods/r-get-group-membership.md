---
description: Gibt die Mitglieder einer Gruppe zurück.
seo-description: Gibt die Mitglieder einer Gruppe zurück.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '87'
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

**Input (getGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Nein | Das Handle für den Benutzer. |
| ` *`companyHandle`*` | `xsd:string` | Nein | Der Griff zur Firma. |

**Output (getGroupMembershipReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Ja | Array von Gruppen. |

## Beispiele {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Dieses Codebeispiel gibt alle Mitglieder einer Gruppe zurück. Da die Firmen- und Benutzergriffe optional sind, kann der Vorgang alle Gruppenmitglieder zurückgeben.

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

