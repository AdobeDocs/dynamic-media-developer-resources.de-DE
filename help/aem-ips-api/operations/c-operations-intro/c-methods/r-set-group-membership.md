---
description: Legt die Gruppenmitgliedschaft für einen Benutzer fest.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
| `*`userHandle`*` | `xsd:string` | Nein | Das Handle des Benutzers, dessen Gruppenmitgliedschaft Sie festlegen möchten. |
| `*`companyHandle`*` | `xsd:string` | Nein | Firma Handle. |
| `*`groupHandleArray`*` | `types:HandleArray` | Ja | Das Array von Handles zu Gruppen, denen der Benutzer angehört. |

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
