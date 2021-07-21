---
description: Fügt Benutzer aus einem bestimmten Unternehmen zu einer bestimmten Gruppe hinzu.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 12%

---

# addGroupMembers{#addgroupmembers}

Fügt Benutzer aus einem bestimmten Unternehmen zu einer bestimmten Gruppe hinzu.

Syntax

## Autorisierte Benutzertypen {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b28434dcf2ca4b4ea431136aac33913e}

**Eingabe (addGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen. |
| `*`groupHandle`*` | `xsd:string` | Ja | Der Gruppengriff. |
| `*`userHandleArray`*` | `types:HandleArray` | Ja | Ein Array von Handles für Benutzer, die Sie einer Gruppe hinzufügen möchten. |

**Ausgabe (addGroupMembersParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-8f168b528aef4c4fa8c3d41f7686842f}

In diesem Beispiel wird `*`addGroupMembersParam`*` verwendet, um einem einzelnen Unternehmen einen Benutzer hinzuzufügen. Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

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
