---
description: Legt die Gruppenmitgliedschaft von Benutzern fest, die zu einer bestimmten Firma gehören.
seo-description: Legt die Gruppenmitgliedschaft von Benutzern fest, die zu einer bestimmten Firma gehören.
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
topic: Scene7 Image Production System API
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setGroupMembers{#setgroupmembers}

Legt die Gruppenmitgliedschaft von Benutzern fest, die zu einer bestimmten Firma gehören.

Der Vorgang gibt einen Authentifizierungsfehler aus, wenn Sie nicht über die erforderlichen Berechtigungen zum Durchführen dieses Vorgangs verfügen. Dies gilt auch dann, wenn einer der Benutzer im user handle-Array nicht zur im Firma-Handle angegebenen Firma gehört,

## Autorisierte Benutzertypen {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`groupHandle`*` | `xsd:string` | Ja | Gruppengriff. |
| ` *`userHandleArray`*` | `types:HandleArray` | Ja | Array von Handles für Benutzer, deren Gruppenmitgliedschaft Sie festlegen möchten. |

**Output (setGroupMembersReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9c528c3f44a141ce9eaddf634f26c487}

In diesem Codebeispiel wird die Gruppenmitgliedschaft für einen einzelnen Benutzer festgelegt.

**Anforderung**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Antwort**

Keine.
