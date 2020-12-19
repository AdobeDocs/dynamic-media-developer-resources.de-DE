---
description: Legt die Gruppenmitgliedschaft für einen Benutzer fest.
seo-description: Legt die Gruppenmitgliedschaft für einen Benutzer fest.
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
topic: Scene7 Image Production System API
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---


# setGroupMembership{#setgroupmembership}

Legt die Gruppenmitgliedschaft für einen Benutzer fest.

Syntax

## Autorisierte Benutzertypen {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Nein | Das Handle des Benutzers, dessen Gruppenmitgliedschaft Sie festlegen möchten. |
| ` *`companyHandle`*` | `xsd:string` | Nein | Firma Handle. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Ja | Das Array von Handles zu Gruppen, denen der Benutzer angehört. |

**Output (setGroupMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-67b86d259df24938896fe19061845811}

Mit diesem Codebeispiel wird der Benutzer zum Mitglied einer Gruppe. hinzufügen einem Benutzer mehrere Gruppen mit dem Gruppen-Handle-Array.

**Anforderung**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Antwort**

Keine.
