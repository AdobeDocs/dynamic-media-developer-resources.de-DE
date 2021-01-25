---
description: Fügt einer bestimmten Firma Benutzer aus einer bestimmten Gruppe hinzu.
solution: Experience Manager
title: addGroupMembers
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---


# addGroupMembers{#addgroupmembers}

Fügt einer bestimmten Firma Benutzer aus einer bestimmten Gruppe hinzu.

Syntax

## Autorisierte Benutzertypen {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b28434dcf2ca4b4ea431136aac33913e}

**Input (addGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| `*`groupHandle`*` | `xsd:string` | Ja | Der Gruppengriff. |
| `*`userHandleArray`*` | `types:HandleArray` | Ja | Ein Array von Handles für Benutzer, die Sie einer Gruppe hinzufügen möchten. |

**Output (addGroupMembersParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-8f168b528aef4c4fa8c3d41f7686842f}

In diesem Beispiel wird `*`addGroupMembersParam`*` verwendet, um einen Benutzer einer einzelnen Firma hinzuzufügen. Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

**Anforderung**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Antwort**

Keine.
