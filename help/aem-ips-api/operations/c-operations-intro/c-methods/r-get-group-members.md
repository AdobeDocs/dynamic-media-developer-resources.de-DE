---
description: Ruft die Benutzer ab, die zu einem bestimmten Unternehmen und einer bestimmten Gruppe gehören.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---

# getGroupMembers{#getgroupmembers}

Ruft die Benutzer ab, die zu einem bestimmten Unternehmen und einer bestimmten Gruppe gehören.

Syntax

## Autorisierte Benutzertypen {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b798b06354c946abbb90fa72cc9c67fd}

**Eingabe (getGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen. |
| `*`groupHandle`*` | `xsd:string` |  | Das Handle für die Gruppe. |

**Ausgabe (getGroupMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Ja | Ein Array von Benutzerhandlern. |

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
