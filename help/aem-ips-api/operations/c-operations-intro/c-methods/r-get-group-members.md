---
description: Ruft die Benutzer ab, die zu einer bestimmten Firma und Gruppe gehören.
seo-description: Ruft die Benutzer ab, die zu einer bestimmten Firma und Gruppe gehören.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Scene7 Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 16%

---


# getGroupMembers{#getgroupmembers}

Ruft die Benutzer ab, die zu einer bestimmten Firma und Gruppe gehören.

Syntax

## Autorisierte Benutzertypen {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b798b06354c946abbb90fa72cc9c67fd}

**Input (getGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| ` *`groupHandle`*` | `xsd:string` |  | Der Griff zur Gruppe. |

**Output (getGroupMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userHandleArray`*` | `type:HandleArray` | Ja | Ein Array von Benutzergriffen. |

## Beispiele {#section-aaa340dba6b64cce9bcd8303cf999166}

Dieses Codebeispiel gibt ein Benutzerhandle-Array zurück, das alle Benutzer enthält, die zu einer bestimmten Gruppe gehören.

**Anforderung**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Antwort**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```

