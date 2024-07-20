---
description: Legt die Gruppenmitgliedschaft von Benutzern fest, die zu einem bestimmten Unternehmen gehören.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 7%

---

# setGroupMembers{#setgroupmembers}

Legt die Gruppenmitgliedschaft von Benutzern fest, die zu einem bestimmten Unternehmen gehören.

Der Vorgang gibt einen Authentifizierungsfehler aus, wenn Sie nicht über die erforderlichen Berechtigungen zum Ausführen dieses Vorgangs verfügen. Dies trifft auch zu, wenn einer der Benutzer im Benutzerhandle-Array nicht zu dem im Unternehmens-Handle angegebenen Unternehmen gehört.

## Autorisierte Benutzertypen {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| groupHandle | `xsd:string` | Ja | Gruppieren. |
| userHandleArray | `types:HandleArray` | Ja | Array von Handles für Benutzer, deren Gruppenmitgliedschaft Sie festlegen möchten. |

**Output (setGroupMemberReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-9c528c3f44a141ce9eaddf634f26c487}

In diesem Codebeispiel wird die Gruppenmitgliedschaft für einen einzelnen Benutzer festgelegt.

**Anfrage**

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
